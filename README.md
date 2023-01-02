# nestjs-app

## Description

[Nest](https://github.com/nestjs/nest) framework TypeScript starter repository.

## Installation

```bash
$ pnpm install
```

## Running the app

```bash
# development
$ pnpm run start

# watch mode
$ pnpm run start:dev

# production mode
$ pnpm run start:prod
```

## Test

```bash
# unit tests
$ pnpm run test

# e2e tests
$ pnpm run test:e2e

# test coverage
$ pnpm run test:cov
```

## Prisma setup

Setup [docker-compose.yml](./docker-compose.yml) and [.env](./.env)

Start the mysql database server

```shell
docker-compose up -d
```

Install prisma

```shell
pnpm install prisma --save-dev
pnpm install @prisma/client
pnpx prisma
pnpx prisma init
```

Add `Customer` model to the [schema.prisma](./prisma/schema.prisma)

Update the `datasource` in [schema.prisma](./prisma/schema.prisma) to use the mysql database

Generate the initial migration script

```shell
pnpx prisma migrate dev --name init
```

Check the database is updated using [phpMyAdmin](http://localhost:8001/)

Start `prisma studio` using the following command

```shell
pnpx prisma studio
```

## References

[Youtube Prisma / Postgres / docker-compose](https://www.youtube.com/watch?v=twi33GVRazE)

[Github Prisma / Postgres / docker-compose](https://github.com/H-Richard/backend-2022)

[Github nestjs-prisma-starter](https://github.com/notiz-dev/nestjs-prisma-starter)
