# Node.js ORMs and Prisma

## What is an ORM?

![ORM](https://res.cloudinary.com/practicaldev/image/fetch/s--pQkm60iG--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/rtim9ih6u0kuxuuvpvp6.png) 

<sub>[Source](https://dev.to/jhonywalkeer/orm-as-melhores-bibliotecas-para-javascript-2pc0)</sub>

Object-Relational Mapping (ORM) is a technique used to map object-oriented programming concepts to a relational database. It's typically used in languages like Java, C#, and Python, where object-oriented programming is a core concept.

However, even in non-object-oriented languages like JavaScript, an ORM can still be useful. In JavaScript, an ORM can be used to provide a high-level API for working with databases that abstracts away the underlying SQL queries and provides an intuitive way to interact with the database using JavaScript code.

## Popular Node.js ORMs

There are several popular ORM libraries in JavaScript that can be used to interact with relational databases when working with a Node.js back-end. Some of the top ones include:

1. `Sequelize`: This is a powerful ORM for Node.js that supports multiple databases, including MySQL, PostgreSQL, SQLite, and Microsoft SQL Server. It provides features like data validation, association management, and transaction support.

2. `TypeORM`: This is another popular ORM for Node.js that supports multiple databases, including MySQL, PostgreSQL, SQLite, and Microsoft SQL Server. It provides features like automatic schema migration, data seeding, and query caching.

3. `Bookshelf.js`: This is a lightweight ORM for Node.js that provides a simple and intuitive API for working with relational databases. It supports MySQL, PostgreSQL, SQLite, and Oracle databases.

4. `Knex.js`: This is a query builder for Node.js that can also be used as an ORM. It supports multiple databases and provides features like query chaining, transactions, and migrations.

5. `Prisma`: This provides a type-safe and intuitive API for working with databases in JavaScript. It uses a schema-based approach to define your data model, and then generates the necessary SQL queries and provides a client-side API to interact with the database using JavaScript code.

## Pick One - Why Prisma?

Here are three reasons why Prisma is gaining popularity - and perhaps why you should pick it!

### 1 - Type-safety and intuitive API 🔒
Prisma provides a type-safe and intuitive API for working with databases. This means that you can write code that is easier to understand, maintain, and debug. 

You can use Prisma to define your database schema in a simple and intuitive way, and then use the generated Prisma client to interact with your database using a type-safe API. This makes it easier to catch errors and enforce constraints at compile-time, rather than discovering them at runtime.

### 2 - High performance and scalability 🚀
Prisma is designed to be fast and scalable. It uses a powerful query engine that can generate optimized SQL queries for maximum performance, and it supports advanced features like batching, caching, and pagination. 

Prisma is also designed to work well with modern cloud-based databases like AWS Aurora or Google Cloud SQL, which can provide high scalability and availability.

### 3 - Flexibility and portability 💼
Prisma is flexible and portable. It supports multiple databases, including popular databases like MySQL, PostgreSQL, and MongoDB. This means that you can use Prisma to work with a variety of databases, depending on the needs of your project. 

Prisma is also designed to be easy to set up and use, which can save you time and effort when developing your project. Finally, Prisma is open source and has a strong community, which means that you can rely on it for ongoing support and development.

## Getting Started with Prisma - 4 Easy Steps

### Step 1 - Install Prisma CLI

```
npm install prisma --save-dev
```

### Step 2 - Define your database schema

Use the `Prisma Schema Definition Language (SDL)` to define your data model, including entities, fields, and relationships. Here's an example schema:

```
datasource db {
  provider = "postgresql"
  url      = env("DATABASE_URL")
}

generator client {
  provider = "prisma-client-js"
}

model User {
  id       Int      @id @default(autoincrement())
  name     String
  email    String   @unique
  password String
  posts    Post[]
}

model Post {
  id        Int      @id @default(autoincrement())
  title     String
  content   String
  authorId  Int
  author    User     @relation(fields: [authorId], references: [id])
}
```

### Step 3 - Generate Prisma client

```
npx prisma generate
```

This will generate a `node_modules/@prisma/client` folder that contains the Prisma client code.

### Step 4 - Use Prisma client in your application

Finally, you can use the Prisma client in your Node.js application to interact with your database using the type-safe API that Prisma provides. Here's an example of how to use the Prisma client to query all users:

```
const { PrismaClient } = require('@prisma/client')

const prisma = new PrismaClient()

async function main() {
  const allUsers = await prisma.user.findMany()
  console.log(allUsers)
}

main()
  .catch(e => console.error(e))
  .finally(async () => await prisma.$disconnect())
```

