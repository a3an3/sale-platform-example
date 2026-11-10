# Sale Platform – Example Website

Example sales website built with **SvelteKit**. It gets its content from my
[Sanity Content Studio](#) and is deployed as a static site.

🔗 **Live:** [https://…](https://…)

## Features

- Responsive landing page with header, product/offer sections and an FAQ section
- Content (texts, FAQ, images) managed in Sanity, no code change needed to update it
- Contact form with email delivery via **SendGrid**
- Static build, deployed on [Vercel]

## Tech stack

SvelteKit · Vite · JavaScript · Sanity (headless CMS) · SendGrid · ESLint · Prettier

## Project structure

| Path | Purpose |
|---|---|
| `src/routes/` | Pages and the server endpoint for the contact form |
| `src/lib/` | Components (header, FAQ, …) and the Sanity client |
| `static/` | Images, favicon and other static assets |

## Getting started

```bash
npm install
npm run dev
