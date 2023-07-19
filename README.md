# create-svelte

Everything you need to build a Svelte project, powered by [`create-svelte`](https://github.com/sveltejs/kit/tree/master/packages/create-svelte).

## Configuration

Create a new project in Supabase

Your project admin dashboard URL will be something like `https://supabase.com/dashboard/project/[unique string here]`

In the repo copy `.env.example` sample file to a `.env` file

Go to `/settings/api` for your Supabase project

Copy the values for `PUBLIC_SUPABASE_URL` and `PUBLIC_SUPABASE_ANON_KEY` from the project to the `.env` file.

In Supabase, go to `Authentication` -> `URL Configuration`

Go to `auth/url-configuration` for your Supabase project

Edit the URL to match the local Supabase server (f.ex `localhost:5173`)

Also add a Redirect url `http://localhost:5173`

## Creating a project

If you're seeing this, you've probably already done this step. Congrats!

```bash
# create a new project in the current directory
npm create svelte@latest

# create a new project in my-app
npm create svelte@latest my-app
```

## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

To create a production version of your app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://kit.svelte.dev/docs/adapters) for your target environment.
