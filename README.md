# Playwright TypeScript Tutorial

A complete tutorial website for learning Playwright with TypeScript, including installation, locators, assertions, API testing, and CI setup.

## Live site

https://Jag1603.github.io/playwright-typescript-tutorial/

## Features

- Beautiful static landing page
- Beginner-friendly learning sections
- TypeScript Playwright examples
- GitHub Pages deployment config
- CI workflow example

## Quick start

```bash
npm init -y
npm install -D @playwright/test typescript
npx playwright test
```

## First example

```ts
import { test, expect } from '@playwright/test';

test('home page loads', async ({ page }) => {
  await page.goto('https://example.com');
  await expect(page).toHaveTitle(/Example/);
  await expect(page.getByRole('heading')).toContainText('Example Domain');
});
```

## GitHub Pages

This repository uses the `docs/` folder for the static website and a GitHub Actions workflow for deployment.

1. Go to Settings → Pages
2. Set source to GitHub Actions
3. Push changes to `main`
4. Your page will deploy automatically
