<div align="center">
  <img alt="Logo" src="src/images/phi.svg" width="100" />
</div>
<h1 align="center">
  AvlasRefl.github.io
</h1>


## 🚨 Forking this repo (please read!)

Yes, you can fork this repo. This repo is also a fork from https://v4.brittanychiang.com/.

## 🛠 Installation & Set Up

1. Install the Gatsby CLI

   ```sh
   npm install -g gatsby-cli
   ```

2. Install and use the correct version of Node using [NVM](https://github.com/nvm-sh/nvm)

   ```sh
   nvm install
   ```

3. Install dependencies

   ```sh
   yarn
   ```

4. Start the development server

   ```sh
   npm start
   ```

## 🚀 Building and Running for Production

1. Deploy to github.io (GitHub Pages)

   ```sh
   npm run deploy
   ```

## ✅ Correct Deploy Flow (this repo)

This repo is a Gatsby site. Source lives on the `source` branch, and the built static site is published to the `main` branch via `gh-pages`.

### Prerequisites

- Node **22.x** (see `.nvmrc`). Newer Node versions may break older Gatsby toolchain.
- GitHub push access to `git@github.com:AvlasRefl/AvlasRefl.github.io.git` (SSH key set up).

### One-time setup

1. Use Node 22

   - If you have `nvm`:

     ```sh
     nvm install
     nvm use
     ```

   - If you don't have `nvm` (Homebrew on macOS):

     ```sh
     brew install node@22
     export PATH="/opt/homebrew/opt/node@22/bin:$PATH"
     ```

2. Enable Yarn (Classic) via Corepack

   ```sh
   corepack enable
   corepack prepare yarn@1.22.22 --activate
   ```

3. Install dependencies

   ```sh
   yarn install
   ```

### Deploy (repeatable)

From the `source` branch:

```sh
git checkout source
git pull
npm run deploy
```

What it does:

- `predeploy`: runs `gatsby build` and outputs to `public/`
- `deploy`: runs `gh-pages -d public -b main` to publish `public/` to the `main` branch

### After deploy

- The site should be served from the `homepage` in `package.json` (currently `https://avlasrefl.github.io`).
- If you changed dependencies, commit `yarn.lock` on `source` so future installs are reproducible.

