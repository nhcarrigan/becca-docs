# Managing the Database

We use [Prisma](https://www.prisma.io/) to manage our MongoDB connection and data. Using Prisma comes with a few important caveats.

## Setting Up The Database

If you are setting up a new MongoDB instance, cluster, or database, you will need to populate the database with the necessary collections. Ensure you have the `MONGODB` environment variable set correctly in your `.env` file, then run:

```bash
npx prisma db push
```

This will prepare the database for use and validate any existing documents.

## Changing the Schema

The schema can be found in `prisma/schema.prisma`. If you make changes to the schema, you will need to generate a new type definition for the database client. To do this, run:

```bash
npx prisma generate
```

To apply the changes to the database, run the `push` command again:

```bash
npx prisma db push
```

> [!TIP]
> Changes to the schema should be committed to version control.

## Pulling From the Database

You can also introspect the database to generate the schema from the existing data. To do this, run:

```bash
npx prisma db pull
```

This will update the `schema.prisma` file to match the existing database - in some cases, Prisma will fail to infer an accurate type. Be sure to check the schema file for comments indicating this.

## Creating a New Model

All models are defined in the `schema.prisma` file. Creating a new model requires a few steps. First, define your model - the name should always be plural:

```prisma
model coolthings {

}
```

Every MongoDB model needs an `_id` value. In Prisma, you declare that as an `id` value and map it to `_id`.

```prisma
model coolthings {
  id       String @id @default(auto()) @map("_id") @db.ObjectId
}
```

Mongoose uses a versioning key, which is present on our existing models. The `@ignore` field keeps it out of Prisma's client and allows us to stop using it.

```prisma
model coolthings {
  id       String @id @default(auto()) @map("_id") @db.ObjectId
  v        Int?   @map("__v") @ignore
}
```

Adding your fields:

```prisma
model coolthings {
  id       String @id @default(auto()) @map("_id") @db.ObjectId
  v        Int?   @map("__v") @ignore
  serverId String @default(0)
  stuffs   Int    @default(0)
}
```

Every model needs at least one unique property to serve as the index.

````prisma
model coolthings {
  id       String @id @default(auto()) @map("_id") @db.ObjectId
  v        Int?   @map("__v") @ignore
  serverId String @default(0)
  stuffs   Int    @default(0)

  @@unique([serverId], map: "serverId_1")
}

But if you want a pair of keys to be unique:

```prisma
model coolthings {
  id       String @id @default(auto()) @map("_id") @db.ObjectId
  v        Int?   @map("__v") @ignore
  serverId String @default(0)
  stuffs   Int    @default(0)
  userId   String @default(0)

  @@unique([serverId, userId], map: "serverId_1_userId_1")
}
````

> [!NOTE]
> This would require that each `serverId-userId` pairing be unique. You could have two documents with `123` as the `serverId`, but they must have different `userId`s.

## Contributing Database Changes

This can all seem overwhelming, and that's okay! Database changes can be very expensive and messy, so it is rare that you'd see an opportunity to contribute a database change.

If you get stuck with the database stuff in your local environment, reach out to us on [Discord](https://chat.nhcarrigan.com) and we may be able to help!
