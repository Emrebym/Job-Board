<div align="center">

# 💼 Job Board

**A full-stack job listing platform built with Next.js 14, Prisma, and Clerk authentication**

![Next.js](https://img.shields.io/badge/Next.js_14-000000?style=flat-square&logo=next.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Clerk](https://img.shields.io/badge/Clerk-6C47FF?style=flat-square&logo=clerk&logoColor=white)

</div>

---

## 📖 About

A production-ready job board application where companies can post job listings and candidates can browse, search, and filter positions. Built with Next.js 14 App Router, Prisma ORM for database management, and Clerk for secure authentication. Features an admin dashboard for managing job approvals.

## ✨ Features

- **Job posting form** — rich text editor (WYSIWYG) for detailed job descriptions with React Draft WYSIWYG
- **Advanced filtering** — filter by job type, location, search keywords
- **Job detail pages** — full descriptions with Markdown rendering via react-markdown
- **Admin dashboard** — approve, reject, or manage submitted job listings
- **Authentication** — secure user auth with Clerk (sign up, sign in, session management)
- **File uploads** — company logo uploads via Vercel Blob storage
- **SEO-friendly** — server-side rendering with Next.js App Router
- **Responsive UI** — built with Tailwind CSS and shadcn/ui components (Radix UI)
- **Database** — Prisma ORM with type-safe database queries

## 🏗️ Architecture

```
src/
├── app/
│   ├── page.tsx                    # Homepage — job listings with filters
│   ├── layout.tsx                  # Root layout with Clerk provider
│   ├── jobs/
│   │   ├── [slug]/page.tsx         # Job detail page with Markdown
│   │   └── new/
│   │       ├── page.tsx            # Job submission page
│   │       └── NewJobForm.tsx      # Form with WYSIWYG editor
│   ├── admin/
│   │   ├── page.tsx                # Admin dashboard
│   │   ├── layout.tsx              # Admin layout with auth guard
│   │   ├── AdminNavbar.tsx         # Admin navigation
│   │   └── jobs/[slug]/
│   │       ├── page.tsx            # Admin job review
│   │       └── AdminSidebar.tsx    # Approve/reject controls
│   └── job-submitted/page.tsx      # Submission confirmation
├── components/
│   ├── JobResults.tsx              # Job listing cards
│   ├── JobFilterSidebar.tsx        # Search & filter sidebar
│   └── Footer.tsx                  # Site footer
└── lib/
    └── prisma.ts                   # Prisma client singleton
```

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Framework | Next.js 14 (App Router, Server Components) |
| Language | TypeScript |
| Database | Prisma ORM |
| Auth | Clerk |
| UI | Tailwind CSS, shadcn/ui (Radix), Lucide icons |
| Forms | React Hook Form + Zod validation |
| Rich Text | React Draft WYSIWYG, react-markdown |
| Storage | Vercel Blob |
| IDs | nanoid |

## 🚀 Getting Started

```bash
git clone https://github.com/Emrebym/Job-Board.git
cd Job-Board
npm install
```

Create a `.env` file with your credentials:

```env
DATABASE_URL="your-database-url"
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY="your-clerk-key"
CLERK_SECRET_KEY="your-clerk-secret"
BLOB_READ_WRITE_TOKEN="your-vercel-blob-token"
```

```bash
npx prisma db push    # Setup database
npm run dev            # Start development server
```

The app will be available at `http://localhost:3000`

## 📝 License

MIT
