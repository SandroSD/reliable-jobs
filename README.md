# reliable-jobs

Code for the blog series **"Reliable background jobs in Node.js, from zero"** by [Sandro Dezerio](https://dev.to/sandrosd).

Each part of the series gets its own folder under `src/` and `test/`, with a demo script that reproduces the numbers shown in that post.

## Setup

```bash
npm install
```

## Part 1 — What is a job queue, and why does my API need one?

A ~40-line in-memory job queue (`src/part01/queue.ts`), plus a simulation comparing a signup endpoint that sends email inline vs. one that queues it (`src/part01/demo.ts`).

```bash
npm run part01:demo   # prints the response-time / error-rate table from the post
npm run part01:test   # runs the unit tests for SimpleQueue
```

Change `SAVE_MS`, `EMAIL_MS`, and `EMAIL_FAIL_RATE` as environment variables to see how the numbers move, e.g.:

```bash
EMAIL_FAIL_RATE=0.3 npm run part01:demo
```

## AI-assistance disclosure

Code in this repository was written with help from Claude for structure and editing, then run and reviewed by hand. All numbers printed by the demo scripts are reproducible by running them yourself — nothing is hardcoded or faked.

## License

MIT
