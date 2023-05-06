# Create T3 App

This is a [T3 Stack](https://create.t3.gg/) project bootstrapped with `create-t3-app`.

## What's next? How do I make an app with this?

We try to keep this project as simple as possible, so you can start with just the scaffolding we set up for you, and add additional things later when they become necessary.

If you are not familiar with the different technologies used in this project, please refer to the respective docs. If you still are in the wind, please join our [Discord](https://t3.gg/discord) and ask for help.

- [Next.js](https://nextjs.org)
- [NextAuth.js](https://next-auth.js.org)
- [Prisma](https://prisma.io)
- [Tailwind CSS](https://tailwindcss.com)
- [tRPC](https://trpc.io)

## Learn More

To learn more about the [T3 Stack](https://create.t3.gg/), take a look at the following resources:

- [Documentation](https://create.t3.gg/)
- [Learn the T3 Stack](https://create.t3.gg/en/faq#what-learning-resources-are-currently-available) — Check out these awesome tutorials

You can check out the [create-t3-app GitHub repository](https://github.com/t3-oss/create-t3-app) — your feedback and contributions are welcome!

## How do I deploy this?

![clever cloud logo](public/clever-cloud-logo.png)

You can deploy this app eiher using a Static runtime or a Node.js runtime.

In both cases, commit the `/.next` repository, otherwise NextJS won't find the build folder on the server. This repository already contains a `.gitignore` file without `.next` folder.

### Steps to deploy on Clever Cloud

Follow this procedure to deploy on Clever Cloud.

#### 1. Declare the app

Click on **Create > an application**, select your preferred deployment method (Git or GitHub intgartion). Select a **Node.js** runtime. An XS size is enough to deploy.

#### 2. Do I need a Database?

This is a demo app, you don't need to add a database. However, if you start working with Prisma and need one, you can migrate your schema dynamically (more on that later).

When prompted with an addon selection, just click on "I don' need any addon".

#### 3. Add variables

Add the following environment variable: `CC_WEBROOT`= `/.next`

You can optionnally set a `NODE_ENV` environment variable if needed.

These are the variables this repository uses. If you use any other in-app variables, don't forget to add it **before** deploying, so the new parameters can be injected.

If you forget, just wait until the deployment is over, add it, and restart the app.

**Don't forget to save changes!**

Notes on environment variables on Clever Cloud**

There is a lot you can do on Clever cloud with environment variables. You can find all the references [in the doc](https://www.clever-cloud.com/doc/reference/reference-environment-variables/).

#### Deploy this app

The Clever Cloud console will prompt you a git command to push your new app, so:

- Clone this repository: `git clone ssh://hg@heptapod.host/tam-shenanigans/t3-app.git`
- Open it: `cd t3-app`
- Copy paste the git commands provided by Clever Cloud

(If you have closed the logs or the page, you can still find the commands on your app menu > **Information**)

Voilà!

**Git tip**: Sometimes, when you clone from GitHub, the default branch is `main`. If `git push clever master` doesn't work, `git push clever main:master` will do the trick. This way, you can even deploy test apps from any branch on Clever Cloud without merging. This is a good way of checking the deployment process as you code.
