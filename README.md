# SST Demo Notes App [![Seed Status](https://api.seed.run/serverless-stack/demo-notes-app/stages/prod/build_badge)](https://console.seed.run/serverless-stack/demo-notes-app)

The [Serverless Stack Guide](https://sst.dev/guide) is a comprehensive open source tutorial for building and deploying full-stack apps using serverless and React on AWS.

We create a [note taking app](https://demo.sst.dev) from scratch. Using React.js, AWS Lambda, API Gateway, DynamoDB, and Cognito.

![Demo App](screenshot.png)

This repo is a full-stack serverless app built with [SST](https://github.com/serverless-stack/sst).

- The `stacks/` directory defines our AWS infrastructure using AWS CDK.
- The `packages/` directory contains the Lambda functions that power the CRUD API.
- The `frontend/` directory contains the React app.

It's a single-page React app powered by a serverless CRUD API. We also cover how add user authentication, handle file uploads, and process credit card payments with Stripe.

### Usage

Clone this repo.

```bash
$ git clone https://github.com/serverless-stack/demo-notes-app
```

Install dependencies.

```bash
$ npm install
```

This project refers to a `.env.local` file with a secret that we are not checking in to the repo. Make sure to create one before deploying - https://sst.dev/chapters/handling-secrets-in-sst.html.

#### Developing Locally

Start the [Live Lambda Dev Environment](https://docs.sst.dev/live-lambda-development).

```bash
$ npx sst dev
```

Install dependencies for the frontend React app.

```bash
$ cd frontend
$ npm install
```

Start the React local dev environment from the `frontend/` dir.

```bash
$ npm start
```

#### Running Tests

From the project root.

```bash
$ npm test
```

#### Deploying to Prod

Run this in the project root to deploy it to prod.

```bash
$ npx sst deploy
```

---

Join the SST community over on [Discord](https://discord.gg/sst) and follow us on [Twitter](https://twitter.com/SST_dev).
