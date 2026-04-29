# Harvest and Collect

Harvest and Collect is a small browser farming game built with Next.js, React, and TypeScript. Players can plant flowers, watch them grow through timed stages, collect crops for profit, and choose which seed to plant from an in-game store.

## Features

- 4x4 interactive farm grid
- Starting balance of `$100`
- Plant growth stages with emoji-based crop states
- Crop collection and balance rewards
- Rotting crops if mature plants are not collected in time
- Flower store with selectable seed types
- Basic sign up and sign in screens backed by browser `localStorage`
- CSS Modules for component-scoped styling

## Tech Stack

- [Next.js](https://nextjs.org/) 15
- [React](https://react.dev/) 19
- [TypeScript](https://www.typescriptlang.org/)
- [Tailwind CSS](https://tailwindcss.com/) 4
- CSS Modules

## Getting Started

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## Available Scripts

```bash
npm run dev
```

Runs the app in development mode with Turbopack.

```bash
npm run build
```

Builds the production version of the app.

```bash
npm run start
```

Starts the production server after a build.

```bash
npm run lint
```

Runs the configured Next.js lint command.

## How to Play

1. Open the game at `/`.
2. Click **Open Store** to choose a flower seed.
3. Click an empty plot to plant the selected seed.
4. Wait for the crop to grow through its stages.
5. Click the mature crop to collect money.
6. Collect quickly, because mature crops rot after a short delay.

Current flower options:

| Flower | Seed Cost | Crop Value |
| --- | ---: | ---: |
| Sunflower | `$10` | `$20` |
| Tulip | `$20` | `$40` |

## Routes

| Route | Description |
| --- | --- |
| `/` | Main farm game |
| `/login` | Welcome screen with sign in and sign up links |
| `/signin` | Sign in form |
| `/signup` | Sign up form |

## Project Structure

```text
src/app
├── components
│   ├── balance
│   ├── box
│   └── store
├── contexts
│   ├── BalanceContext.tsx
│   └── FlowerStoreContext.tsx
├── login
├── signin
├── signup
├── globals.css
├── layout.tsx
└── page.tsx
```

## Notes

- Authentication is currently client-side only and stores users in `localStorage`. It is useful for prototyping, but it is not secure for production.
- Game state resets when the page reloads.
- `src/app/page.module.css` references `/farm-bg.png`; add that image to the app's public assets if you want the farm background to render.
