# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Webflow Cloud boilerplate project created with the official Webflow CLI. It's built with Next.js 15, React 19, and configured for deployment on Cloudflare Workers using OpenNext.js.

## Technology Stack

- **Framework**: Next.js 15.2.5 with App Router
- **Language**: TypeScript 5
- **Styling**: Tailwind CSS 4
- **Deployment**: Cloudflare Workers with OpenNext.js
- **Integration**: Webflow DevLink for design system components

## Key Commands

### Development
- `npm run dev` - Start development server (localhost:3000)
- `npm run build` - Build Next.js application
- `npm run start` - Start production server
- `npm run lint` - Run ESLint

### Deployment
- `npm run deploy` - Build and deploy to Cloudflare Workers
- `npm run preview` - Build and preview locally
- `npm run cf-typegen` - Generate Cloudflare types

### Webflow Integration
- `npx webflow devlink sync` - Sync DevLink components from Webflow

## Project Structure

```
├── src/
│   ├── app/                 # Next.js App Router
│   │   ├── globals.css      # Global styles with Tailwind
│   │   ├── layout.tsx       # Root layout with DevLink provider
│   │   └── page.tsx         # Home page using DevLink components
├── devlink/                 # Auto-generated Webflow components
├── public/                  # Static assets
├── webflow.json            # Webflow Cloud configuration
├── wrangler.jsonc          # Cloudflare Workers configuration
├── open-next.config.ts     # OpenNext.js configuration
└── next.config.ts          # Next.js configuration
```

## Configuration Files

- **webflow.json**: Defines framework and DevLink settings
- **wrangler.jsonc**: Cloudflare Workers deployment configuration
- **open-next.config.ts**: OpenNext.js adapter configuration
- **next.config.ts**: Next.js configuration with base path for Cloudflare

## DevLink Integration

The project includes DevLink integration for Webflow components:
- Components are imported from `../../devlink`
- Layout includes `DevLinkProvider` wrapper
- Global DevLink styles are imported in layout

## Development Notes

- **Node.js**: Uses modern Node.js features
- **React**: Uses React 19 with latest features
- **Cloudflare**: Configured for Cloudflare Workers deployment
- **DevLink**: Auto-synced components from Webflow design system
- **TypeScript**: Includes Cloudflare Workers types

## Deployment

The project is configured for automatic deployment to Webflow Cloud:
1. Code is built using Next.js
2. OpenNext.js adapter prepares it for Cloudflare Workers
3. Deployed via Webflow Cloud infrastructure

## Prerequisites

- Node.js (latest LTS)
- npm package manager
- Webflow account for DevLink sync
- Cloudflare account for Workers deployment