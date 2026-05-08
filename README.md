щоб створити бд, вводиом це:
docker run --name some-postgres -e POSTGRES_PASSWORD=password -p 5432:5432 -d postgres:18.3

потім у DBeaver у полі password вводимо password

потім
CREATE EXTENSION IF NOT EXISTS "uuid-ossp";

CREATE TABLE books (
    id UUID PRIMARY KEY DEFAULT uuid_generate_v4(),
    title TEXT NOT NULL,
    author TEXT NOT NULL,
    year INTEGER NOT NULL,
    price DECIMAL(10, 2) NOT NULL
);