# Decisions

I want to document the rationale behide the project decisions. I'll try to keep this up-to-date.

## Repo

### [pnpm](https://pnpm.io/)

> TLTR: It saves disk space and it's fast

Great option if you have a lot of projects from the same ecosystem, Typescript/Node for example, because it doesn't let you have duplicated dependencies, it checks for previously downloaded dependencies in pnpm cache to be more disk-efficient.

### [pnpm workspaces](https://pnpm.io/workspaces)

Since I'm using pnpm and I want to build multiple packages/apps it just make sense to use it.

## Formater and code style

### [Biomejs](https://biomejs.dev/)

> TLTR: I don't want to fix Prettier + Eslint compatibilities issues

Prettier + Eslint it's cool, I've been using this combo for a while and usually works until it doesn't.
Biomejs it's a all-in-one option, fixing the compatibility issue, and keeping both the formatter and code lint configuration in one place.
Also, great initial default options, easy installation process and great monorepo support.

## Stack

### [Typescript](https://www.typescriptlang.org/)

Because developing in pure Javascript is a hahazardous work

### [Bun](https://bun.com) (Node)

> TLTR: Node seems good for a open-source project. Bun is fast and comes with bult-in tools

Node works great for I/O-bound apps, it's widely adopted and has a huge open-source community.

A common use case for a LMS is to save users progress when they are watching the lesson, and users will be wathcing lessons simultaneously, so Lemes must handle thousands of requests per send with a fast response time, that's where Bun comes in as the fastest Javascript runtime according to benchmarks, [Anton Putra has an amazing benchmark video](https://www.youtube.com/watch?v=_iEaaNIjg7U), and not only that Bun has a built-in test runner and bundler. So it's the whole toolkit to build modern Javascript apps.
