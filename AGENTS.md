# Agent Guide for my-bingo-mixer

This repository is a React + TypeScript + Vite app using Tailwind CSS v4. It is a social bingo game built as a small frontend workshop project.

## What matters

- `npm install` installs dependencies
- `npm run dev` starts the local app at `http://localhost:5173`
- `npm run build` produces a production bundle via `tsc -b && vite build`
- `npm run lint` validates code with ESLint
- `npm run test` runs Vitest with `jsdom`

## Key source areas

- `src/App.tsx` — root shell and screen routing
- `src/components/` — UI components (`StartScreen`, `GameScreen`, `BingoBoard`, `BingoModal`, `BingoSquare`)
- `src/hooks/useBingoGame.ts` — game state, actions, bingo modal logic
- `src/utils/bingoLogic.ts` — board generation, toggle, bingo detection logic
- `src/data/questions.ts` — question pool used for bingo squares
- `src/index.css` — Tailwind v4 CSS entrypoint and theme tokens
- `vite.config.ts` — Vite config with `@vitejs/plugin-react`, Tailwind plugin, and GitHub Pages base path support

## Development guidance

- Prefer small, incremental changes and preserve existing component structure
- Keep styling in Tailwind v4 CSS using `@import "tailwindcss"` and `@theme`
- Use data-driven logic in `useBingoGame` and `bingoLogic.ts` rather than hard-coded UI behavior
- Keep the bingo rules simple and readable; the workshop is focused on UX and game flow, not complex state machines

## Existing workspace instructions

- `.github/instructions/frontend-design.instructions.md` — frontend design heuristics
- `.github/instructions/tailwind-4.instructions.md` — Tailwind v4 patterns and best practices
- `.github/agents/` — task-specific agent definitions for TDD, UI review, quiz creation, etc.

## Useful notes

- The app uses React 19 and TypeScript 5.9
- Tailwind is configured via Vite plugin and CSS imports, not via `tailwind.config.js`
- `vite.config.ts` sets `base` from `VITE_REPO_NAME` for GitHub Pages deployment
- Tests are isolated to `src/utils/bingoLogic.test.ts` and use Vitest with setup file `src/test/setup.ts`

> Link to workshop docs when the task involves learning or teaching instead of implementing: `workshop/GUIDE.md`, `workshop/01-setup.md`, `workshop/02-design.md`, `workshop/03-quiz-master.md`, `workshop/04-multi-agent.md`.
