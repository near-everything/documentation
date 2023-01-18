---
sidebar_position: 1
---

# setting up the project

In order to run the playground locally and successfully interact with all functionalities, you will need three things running:

## everything api

1. Clone the [everything api repo](https://github.com/near-everything/api).
2. Ensure you have applied the provided .env variables.

```bash
POSTGRES_USER=postgres
POSTGRES_PASSWORD=changeme
POSTGRES_DATABASE=everything
POSTGRES_HOSTNAME=localhost
POSTGRES_PORT=5432

ENABLE_GRAPHIQL=1

COMPOSE_PROJECT_NAME=everything

DATABASE_URL='postgres://postgres:changeme@localhost:5432/everything'
AUTH_DATABASE_URL='postgres://postgres:changeme@localhost:5432/everything'

ISSUER_BASE_URL=
AUDIENCE=

ACCESS_KEY=
SECRET_KEY=
BUCKET_NAME=
```

3. Then:

```bash
  npm install
  npm run docker:up
  npm run dev
```

This will install packages, initialize the postgreSQL database, generate the graphQL schema, and start the api.

The api should be served at localhost:4050.

## everything mesh

1. Clone the [everything mesh repo](https://github.com/near-everything/mesh).
2. Ensure you have applied the provided .env variables.

```bash
EVERYTHING_URL=http://localhost:4050/graphql
```

3. Then:

```bash
  npm install
  npm run dev
```

This will start the mesh of the Mintbase Indexer and the everything api. This is what the playground interacts with.

The mesh should be served at localhost:4000.

## everything playground

1. Clone the [everything-sdk-js repo](https://github.com/near-everything/everything-sdk-js).
2. Ensure you have applied the provided .env variables.

```bash
NEXT_PUBLIC_EVERYTHING_API_URL=http://localhost:4000/graphql

MINTBASE_API_KEY=
NEAR_NETWORK=testnet
NEAR_DATA_ENV=testnet

AUTH0_SECRET=
AUTH0_BASE_URL='http://localhost:3050'
AUTH0_ISSUER_BASE_URL=
AUTH0_CLIENT_ID=
AUTH0_CLIENT_SECRET=
AUTH0_AUDIENCE=
```

3. Then:

```bash
  npm install
  npm run dev
```

This will build the sdk and start the playground.

The playground will be served at localhost:3050.
