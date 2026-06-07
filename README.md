# OpenTerminal

OpenTerminal is a small monorepo containing a CLI-focused frontend package that demonstrates a compact, component-driven terminal UI built with React and OpenTUI components.

## Features

- Component-based terminal UI (`packages/cli`) with header, input bar, status bar, and command menu
- Built using `react` and `@opentui/*` UI primitives
- Fast development workflow with `bun` watch scripts

## Prerequisites

- Install Bun: https://bun.sh/
- Node/TypeScript (for building or type checking) — TypeScript ^5 is used as a peer dependency

## Quickstart

From the repository root you can run the CLI package in watch/dev mode:

```sh
# from repo root
bun run dev:cli
```

Alternatively run the package script directly:

```sh
cd packages/cli
bun run dev
```

This runs the entry file at `packages/cli/src/index.tsx` in watch mode so UI changes reload immediately.

## Project layout

- `packages/cli/` — main frontend package for the terminal UI
  - `src/index.tsx` — app entry
  - `src/components/` — small UI components: `border.tsx`, `header.tsx`, `input-bar.tsx`, `status-bar.tsx`
  - `src/components/command-menu/` — command menu and helpers (`commands.tsx`, `filter-commands.ts`, `use-command-menu.ts`)
  - `src/providers/toast/` — small toast provider used by the UI

## Development notes

- The repository uses Bun for dev scripts (`bun run --watch ...`) for fast startup and file watching.
- Dependencies for the CLI package are declared in `packages/cli/package.json` (React + OpenTUI).
- TypeScript is used — run type checks using your preferred TypeScript tooling if needed.

## Contributing

- Open an issue to discuss major changes.
- Create a branch for your feature or bugfix, then open a pull request.

## License

This project does not currently declare a license. Add a `LICENSE` file if you intend to open-source it.

---

If you'd like, I can also:

- add runnable npm/bun scripts for building and publishing
- add a `dev` README inside `packages/cli` with component docs
- initialize a `LICENSE` and CODE_OF_CONDUCT

Tell me which of those you'd like me to do next.
