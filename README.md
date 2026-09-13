# hono-workers-starter

This is a template based on the [Hono](https://hono.dev/) Cloudflare Workers starter, extended with the following packages.

| Package | Purpose |
| --- | --- |
| [drizzle-orm](https://orm.drizzle.team/) | TypeScript ORM |
| [valibot](https://valibot.dev/) | Schema validation |
| [drizzle-valibot](https://orm.drizzle.team/docs/valibot) | Generates valibot schemas from Drizzle table definitions |

## Setup

```txt
npm install
npm run dev
```

```txt
npm run deploy
```

[For generating/synchronizing types based on your Worker configuration run](https://developers.cloudflare.com/workers/wrangler/commands/#types):

```txt
npm run cf-typegen
```

Pass the `CloudflareBindings` as generics when instantiating `Hono`:

```ts
// src/index.ts
const app = new Hono<{ Bindings: CloudflareBindings }>()
```
