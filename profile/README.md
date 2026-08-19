<h1 align="center">Api-Wrappers</h1>

<p align="center">
  Type-safe TypeScript SDKs for media, anime, gaming, and entertainment APIs.
</p>

<p align="center">
  <a href="https://github.com/Api-Wrappers/anilist-wrapper/stargazers"><img alt="AniList stars" src="https://img.shields.io/github/stars/Api-Wrappers/anilist-wrapper?label=AniList&style=flat"></a>
  <a href="https://github.com/Api-Wrappers/tmdb-wrapper/stargazers"><img alt="TMDB stars" src="https://img.shields.io/github/stars/Api-Wrappers/tmdb-wrapper?label=TMDB&style=flat"></a>
  <a href="https://github.com/Api-Wrappers/igdb-wrapper/stargazers"><img alt="IGDB stars" src="https://img.shields.io/github/stars/Api-Wrappers/igdb-wrapper?label=IGDB&style=flat"></a>
  <a href="https://github.com/Api-Wrappers/trakt-wrapper/stargazers"><img alt="Trakt stars" src="https://img.shields.io/github/stars/Api-Wrappers/trakt-wrapper?label=Trakt&style=flat"></a>
</p>

Api-Wrappers builds focused TypeScript clients for APIs developers regularly reach for when building anime trackers, movie apps, game databases, watch-history tools, and similar projects.

The wrappers aim to remove repetitive integration work without hiding the upstream API. You still get the provider's domain model, plus typed methods, auth helpers, pagination, retries, structured errors, and low-level escape hatches where they make sense.

## Start Here

| Package | Use it for | Install |
| --- | --- | --- |
| [`@api-wrappers/anilist-wrapper`](https://github.com/Api-Wrappers/anilist-wrapper) | Anime, manga, characters, staff, users, media lists, and raw AniList GraphQL | `bun add @api-wrappers/anilist-wrapper` |
| [`@api-wrappers/tmdb-wrapper`](https://github.com/Api-Wrappers/tmdb-wrapper) | Movies, TV, people, search, discover, images, watch providers, sessions, and accounts | `bun add @api-wrappers/tmdb-wrapper` |
| [`@api-wrappers/igdb-wrapper`](https://github.com/Api-Wrappers/igdb-wrapper) | Game metadata, typed APICalypse queries, Twitch auth, pagination, and images | `bun add @api-wrappers/igdb-wrapper` |
| [`@api-wrappers/trakt-wrapper`](https://github.com/Api-Wrappers/trakt-wrapper) | Watchlists, history, ratings, scrobbling, calendars, OAuth, and sync | `bun add @api-wrappers/trakt-wrapper` |
| [`@api-wrappers/api-core`](https://github.com/Api-Wrappers/api-core) | Shared HTTP runtime for building API clients with retries, plugins, auth, caching, and GraphQL helpers | `bun add @api-wrappers/api-core` |

npm, pnpm, and Yarn can be used instead of Bun where the package runtime supports them.

## Useful Combinations

**Movie or TV app**

Use [`tmdb-wrapper`](https://github.com/Api-Wrappers/tmdb-wrapper) for metadata, artwork, search, discovery, and watch-provider data, then pair it with [`trakt-wrapper`](https://github.com/Api-Wrappers/trakt-wrapper) for watchlists, history, ratings, scrobbling, and account sync.

**Anime or manga app**

Use [`anilist-wrapper`](https://github.com/Api-Wrappers/anilist-wrapper) for media discovery, characters, staff, user lists, list mutations, generated GraphQL types, and custom GraphQL operations.

**Game database or discovery app**

Use [`igdb-wrapper`](https://github.com/Api-Wrappers/igdb-wrapper) for typed IGDB queries, filters, pagination, Twitch authentication, and image helpers.

**Building another API client**

Use [`api-core`](https://github.com/Api-Wrappers/api-core) instead of rebuilding request execution, retries, timeouts, auth plugins, rate-limit handling, structured errors, GraphQL requests, and transport hooks.

## What You Get

- TypeScript-first request and response types
- Provider-specific APIs instead of one generic abstraction
- Auth, pagination, retries, timeouts, and structured errors where needed
- ESM/CJS packaging across the SDKs
- Raw request or GraphQL escape hatches for API features the wrapper has not modeled yet
- Runnable examples and contribution guides in the package repositories

## Find More SDKs

[`awesome-api-wrappers`](https://github.com/Api-Wrappers/awesome-api-wrappers) is our curated list of API wrappers and SDKs across TypeScript, Python, Go, Rust, and other ecosystems. It includes both official and community-maintained projects and is open to contributions.

## Contributing

Issues and pull requests are welcome. Good contributions include endpoint coverage, stronger types, practical examples, upstream API compatibility fixes, documentation improvements, and additions to the curated wrapper list.

Pick the package closest to what you want to work on and check its `CONTRIBUTING.md` first.

If one of these packages saves you time, starring its repository helps other developers find it.
