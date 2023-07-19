# Sveltekit Supabase Authentication

A sample app setup with basic username/password login and Social login via multiple OAuth providers.

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

### OAuth configuration for Social login

Go to Supbase dashboard `Authentication` -> `Providers` at `auth/providers`

Enable the Oauth providers of your choice, such as Github and Google.

#### Github Oauth config

Copy the Callback URL from supabase Github Oauth config such as `https://<your project code here>.supabase.co/auth/v1/callback`

For the client id and secret, go to your [Github developer settings](https://github.com/settings/developers) which can be found under your profile icon, `Settings` (ie. `settings/profile`) then `Developer settings` all the way at the bottom which takes you to `settings/apps`. From there click on `OAuth apps`

In the form, register the following:

- Name: `sveltekit-supabase-auth`
- URL: `http://localhost:5173`
- Callback URL: Past the Callback URL from Supabase Github OAuth provider

Click `Register application`

Click to generate a new key. When you have both the Client ID and secret key, transfer these to Supabase OAuth config.

Take the Client ID of the OAuth application and copy/paste back into the Supabase Github OAuth provider configuration. Do the same for the secret. Click `save`

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
