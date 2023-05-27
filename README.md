# sveltekit-adapter-deno

[Adapter](https://kit.svelte.dev/docs/adapters) for [SvelteKit](https://kit.svelte.dev/) apps that generates a standalone [Deno](https://deno.com/runtime) or [Deno Deploy](https://deno.com/deploy) server.

## Usage

Install in your SvelteKit project:

```sh
npm install --save-dev sveltekit-adapter-deno
```

Add the adapter to your [SvelteKit configuration](https://kit.svelte.dev/docs/configuration).

👉 Set `denoDeploy` to `true` if you're deploying to **Deno Deploy**.

```js
// svelte.config.js
import adapter from 'sveltekit-adapter-deno';

/** @type {import('@sveltejs/kit').Config} */
const config = {
  kit: {
    adapter: adapter({
      denoDeploy: true
    })
  }
};

export default config;
```

Build the app for production (`npm run build`).

Serve with **Deno**:

```sh
deno run --allow-env --allow-read --allow-net build/mod.ts
```

Or with **Deno Deploy** set the `entrypoint` to `build/mod.ts`.

## Demo App

This repo publishes a SvelteKit demo app to Deno Deploy at:

[sveltekit-adapter-deno.deno.dev](https://sveltekit-adapter-deno.deno.dev/)

See the [GitHub Action workflow](/.github/workflows/ci.yml) for automated deployment.

* * *

[MIT License](/LICENSE) | Copyright © 2023 [David Bushell](https://dbushell.com)
