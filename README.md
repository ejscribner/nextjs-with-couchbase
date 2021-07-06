## Example app using Couchbase

[Couchbase](https://www.couchbase.com/) is The Modern Database for Enterprise Applications. This example will show you how to connect to and use Couchbase for your Next.js app.

If you want to learn more about Couchbase, visit the following pages:

- [Couchbase Docs](https://docs.couchbase.com/)
- [Couchbase Developer Portal](https://developer.couchbase.com/)
- [Couchbase Cloud](https://cloud.couchbase.com/sign-up)

_NOTE:_ Some parts of this README have been commented out as they apply to Vercel deployment features or create-next-app features that have not yet been configured for Couchbase.

## Deploy your own

Once you have access to the environment variables you'll need, deploy the example using [Vercel](https://vercel.com?utm_source=github&utm_medium=readme&utm_campaign=next-example):
_NOTE:_ direct deployment button is currently unavailable. To deploy a NextJS site to Vercel, clone the project and follow the deployment instructions at the bottom of this README

[comment]: <> (Todo: update this with a new deploy button)
[comment]: <> ([![Deploy with Vercel]&#40;https://vercel.com/button&#41;]&#40;https://vercel.com/new/git/external?repository-url=https://github.com/vercel/next.js/tree/canary/examples/with-mongodb&project-name=with-mongodb&repository-name=with-mongodb&env=MONGODB_URI,MONGODB_DB&envDescription=Required%20to%20connect%20the%20app%20with%20MongoDB&#41;)

## How to use
- Clone this repo and follow configuration steps below
- `create-next-app` support with built in example is pending

[comment]: <> (Note: the bootstrapping instructions below require the `with-couchbase` example to exist &#40;it does not currently&#41;)

[comment]: <> (Execute [`create-next-app`]&#40;https://github.com/vercel/next.js/tree/canary/packages/create-next-app&#41; with [npm]&#40;https://docs.npmjs.com/cli/init&#41; or [Yarn]&#40;https://yarnpkg.com/lang/en/docs/cli/create/&#41; to bootstrap the example:)

[comment]: <> (```bash)

[comment]: <> (npx create-next-app --example with-couchbase with-couchbase-app)

[comment]: <> (# or)

[comment]: <> (yarn create next-app --example with-couchbase with-couchbase-app)

[comment]: <> (```)

## Configuration

### Set up a Couchbase instance

Set up a Couchbase database either locally or with [Couchbase Cloud](https://cloud.couchbase.com/sign-up).

Local installation can be accomplished through a variety of methods, but [Docker](https://docs.couchbase.com/server/current/install/getting-started-docker.html) is the simplest.

After Couchbase is installed, set up a cluster using [this tutorial](https://docs.couchbase.com/server/current/manage/manage-nodes/create-cluster.html). _NOTE:_ the **eventing** and **analytics** services can be unchecked if memory is a constraint (this is often the case with docker and other local installations).

A variety of sample buckets can be installed to get up and running with a data model quickly. We've built an example query based on the `travel-sample`. 
### Set up environment variables

Copy the `env.local.example` file in this directory to `.env.local` (which will be ignored by Git):

```bash
cp .env.local.example .env.local
```

Set each variable on `.env.local`:

- `COUCHBASE_USERNAME` - The username of an authorized user on your Couchbase instance
- `COUCHBASE_PASSWORD` - The corresponding password for the user specified above

### Run Next.js in development mode

```bash
npm install
npm run dev

# or

yarn install
yarn dev
```

Your app should be up and running on [http://localhost:3000](http://localhost:3000)! If it doesn't work, post on [GitHub discussions](https://github.com/vercel/next.js/discussions).

You will either see a message stating "You are connected to Couchbase" or "You are NOT connected to Couchbase". Ensure that you have provided the correct `COUCHBASE_USERNAME` and `COUCHBASE_PASSWORD` environment variables.

When you are successfully connected, you can refer to the [Couchbase Node.js SDK docs](https://docs.couchbase.com/nodejs-sdk/current/hello-world/start-using-sdk.html) for further instructions on how to query your database.

_NOTE_: this project is pre-populated with a test query. If you have loaded the `travel-sample` bucket, the query will run successfully, and you should see list of airlines on the index page. 

## Deploy on Vercel

You can deploy this app to the cloud with [Vercel](https://vercel.com?utm_source=github&utm_medium=readme&utm_campaign=next-example) ([Documentation](https://nextjs.org/docs/deployment)).

#### Deploy Your Local Project

To deploy your local project to Vercel, push it to GitHub/GitLab/Bitbucket and [import to Vercel](https://vercel.com/new?utm_source=github&utm_medium=readme&utm_campaign=next-example).

**Important**: When you import your project on Vercel, make sure to click on **Environment Variables** and set them to match your `.env.local` file.

[comment]: <> (#### Deploy from Our Template)

[comment]: <> (Alternatively, you can deploy using our template by clicking on the Deploy button below.)

[comment]: <> ([![Deploy with Vercel]&#40;https://vercel.com/button&#41;]&#40;https://vercel.com/new/git/external?repository-url=https://github.com/vercel/next.js/tree/canary/examples/with-mongodb&project-name=with-mongodb&repository-name=with-mongodb&env=MONGODB_URI,MONGODB_DB&envDescription=Required%20to%20connect%20the%20app%20with%20MongoDB&#41;)




