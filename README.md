## Blog-Backend-REST-API-NestJS-Prisma 

A simple backend REST API for a blog built using NestJS, Prisma, PostgreSQL and Swagger. 

## Docs

- https://www.prisma.io/blog/nestjs-prisma-rest-api-7D056s1BmOL0

### Installation
1. Install dependencies: `npm install`
2.  Install  SQLite

```
  npm install --save sqlite3
```
* prisma/schema.prisma
```
datasource db {
  # provider = "postgresql"
  provider = "sqlite"
  url      = env("DATABASE_URL")
}
```
3. Start a PostgreSQL database with docker using: 

```
docker-compose up -d
```
    - If you have a local instance of PostgreSQL running, you can skip this step. In this case, you will need to change the `DATABASE_URL` inside the `.env` file with a valid [PostgreSQL connection string](https://www.prisma.io/docs/concepts/database-connectors/postgresql#connection-details) for your database. 
4. Apply database migrations: 
``` 
npx prisma migrate dev
```
5. Start the project:  
```
npm run start:dev
```
6. Access the project at http://localhost:3000/api
