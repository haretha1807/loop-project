# Project LOOP

Project LOOP is a multi-tenant AI customer-feedback intelligence platform.

## Module 1: Foundation

The foundation uses Next.js 14 App Router, TypeScript, Tailwind CSS, PostgreSQL, Prisma, and Auth.js credentials authentication.

### Local setup

1. Copy `.env.example` to `.env` and set `DATABASE_URL` and `NEXTAUTH_SECRET`.
2. Ensure PostgreSQL has the `vector` extension available.
3. Install dependencies with `npm install`.
4. Generate Prisma Client with `npm run db:generate`.
5. Create the first migration with `npm run db:migrate -- --name init`.
6. Start the application with `npm run dev`.

Authentication credentials require `email`, `password`, and `workspaceId`. Session data includes the authenticated user's `workspaceId` and `role`. Application queries must use that session workspace ID as their tenant filter.

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
