<h1 align="center">Api-Wrappers</h1>

<p align="center">
  Type-safe TypeScript SDKs for entertainment, media, anime, and gaming APIs.
</p>

<p align="center">
  <a href="https://github.com/Api-Wrappers"><img alt="TypeScript SDKs" src="https://img.shields.io/badge/TypeScript-SDKs-3178c6?logo=typescript&logoColor=white"></a>
  <a href="https://github.com/Api-Wrappers/api-core/blob/main/LICENSE"><img alt="MIT licensed packages" src="https://img.shields.io/badge/license-MIT-green"></a>
</p>

Api-Wrappers is a collection of focused TypeScript clients for APIs that show up often in media apps, watch tracking tools, anime and manga projects, game databases, and SDK-heavy developer workflows.

The goal is simple: make upstream APIs easier to use without hiding how they work. Each wrapper keeps the provider's domain model visible, adds TypeScript-friendly ergonomics, and shares a consistent request foundation where it makes sense.

## Why Api-Wrappers?

- **Type-safe APIs**: clients expose typed endpoint methods, query inputs, and response shapes so application code can stay closer to the domain.
- **Shared request runtime**: wrappers are built around `@api-wrappers/api-core` for consistent request execution, custom transports, plugin hooks, and response handling.
- **Operational defaults**: retries, timeouts, auth helpers, rate-limit handling, and structured errors are handled in one place instead of being reimplemented per package.
- **Pagination support**: packages expose pagination helpers or pagination metadata for APIs where paged responses are part of the normal workflow.
- **Modern TypeScript packaging**: packages publish TypeScript declarations and ESM/CJS builds for Node projects; Bun is supported where the package docs and runtime requirements call it out.
- **Readable escape hatches**: typed clients are the default, but low-level requests, raw GraphQL, or provider-specific query syntax remain available when the API moves faster than the wrapper.

## Packages

| Package | API / project | Best for | Runtime notes |
| --- | --- | --- | --- |
| [`@api-wrappers/api-core`](https://github.com/Api-Wrappers/api-core) | Shared HTTP runtime | Request orchestration, retries, timeouts, auth plugins, cache/rate-limit plugins, GraphQL helpers, custom transports, and structured errors. | Node 18+, Bun, browsers, edge runtimes, or any runtime with `fetch`, `Request`, `Response`, and `AbortController`. |
| [`@api-wrappers/tmdb-wrapper`](https://github.com/Api-Wrappers/tmdb-wrapper) | [TMDB](https://www.themoviedb.org/) | Movies, TV, people, search, discover, images, watch providers, sessions, account workflows, and TMDB v3 endpoint coverage. | TypeScript package with ESM/CJS builds; package metadata declares Node 16+ and the README documents Node and Bun usage. |
| [`@api-wrappers/trakt-wrapper`](https://github.com/Api-Wrappers/trakt-wrapper) | [Trakt](https://trakt.tv/) | Watch history, watchlists, ratings, lists, calendars, scrobbling, OAuth flows, sync workflows, and paginated Trakt responses. | TypeScript package with ESM/CJS builds; Node 18+ and Bun-oriented development scripts. |
| [`@api-wrappers/igdb-wrapper`](https://github.com/Api-Wrappers/igdb-wrapper) | [IGDB](https://www.igdb.com/) | Typed APICalypse queries, fluent field selection, filters, pagination, Twitch auth, image helpers, protobuf, multi-query, and raw IGDB requests. | TypeScript package with ESM/CJS builds; Node 18+ and Bun-oriented development scripts. |
| [`@api-wrappers/anilist-wrapper`](https://github.com/Api-Wrappers/anilist-wrapper) | [AniList](https://anilist.co/) | Anime, manga, characters, staff, users, media lists, authenticated list mutations, generated GraphQL types, and raw GraphQL access. | TypeScript package with ESM/CJS builds for Node applications; examples and scripts use Bun. |
| [`awesome-api-wrappers`](https://github.com/Api-Wrappers/awesome-api-wrappers) | Curated list | A selective catalog of API wrappers and SDKs with clear docs, active maintenance signals, useful coverage, and idiomatic interfaces. | Documentation project, not a runtime SDK. |

## Shared Ecosystem

The wrappers are designed to feel related without forcing every API into the same shape.

`@api-wrappers/api-core` provides the common foundation: request execution, query serialization, retries, timeouts, auth helpers, structured `ApiError` / `RateLimitError` / `TimeoutError` handling, plugin lifecycle hooks, GraphQL requests, custom fetch or transport support, and typed response helpers.

Domain packages then layer provider-specific behavior on top:

- TMDB keeps movie, TV, search, image, account, and discovery workflows grouped by endpoint area.
- Trakt exposes OAuth helpers, sync actions, scrobbling, calendars, list management, and pagination metadata from response headers.
- IGDB focuses on fluent typed APICalypse queries, endpoint discovery, pagination, images, and Twitch credential management.
- AniList combines convenience services for common anime/manga workflows with generated GraphQL types and raw GraphQL access.

## Best Use Cases

- Building media discovery apps that need TMDB metadata, images, search, and watch-provider data.
- Adding Trakt watch history, watchlists, ratings, scrobbling, or user sync to a movie and TV app.
- Querying IGDB for game metadata with typed field selection, filters, and paginated result sets.
- Building anime or manga tools around AniList data, user lists, authenticated mutations, and GraphQL workflows.
- Creating new API clients that should share a tested HTTP runtime instead of rebuilding retries, auth, timeouts, and error handling.
- Finding well-maintained SDKs across languages through the curated `awesome-api-wrappers` list.

## Contributing

Contributions are welcome when they keep the packages accurate, typed, and maintainable.

Good contributions usually fall into one of these areas:

- filling API coverage gaps with typed endpoint methods
- improving generated or hand-written TypeScript types
- adding focused examples for real workflows
- tightening docs around auth, pagination, request config, or error handling
- fixing upstream API changes
- improving shared runtime behavior in `@api-wrappers/api-core`
- adding high-quality entries to `awesome-api-wrappers`

Before opening a pull request, check the target repository's README and contribution notes. Package repos generally include Bun-based validation scripts for tests, typechecking, formatting, and builds.

## Roadmap

The current direction is practical and package-driven:

- keep wrapper APIs aligned with upstream API changes
- continue moving shared request behavior into `@api-wrappers/api-core`
- expand typed endpoint coverage where real workflows still require raw requests
- improve examples for auth-heavy and pagination-heavy use cases
- keep documentation consistent across packages
- strengthen release quality gates around types, builds, tests, and package contents

No adoption numbers, benchmarks, or production claims are implied here. The repositories are intended to stand on their published packages, tests, examples, and documentation.
