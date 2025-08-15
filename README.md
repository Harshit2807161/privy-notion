# Privy Notion

A **collaborative text-editing workspace** with **real-time editing** powered by [Socket.IO](https://socket.io/) and [Next.js](https://nextjs.org/).  
Privy Notion allows multiple users to edit the same document simultaneously while seeing each other’s changes and cursor positions live.

---

## Features

- **Real-time Collaboration** – Multiple users can edit the same document in sync.
- **Live Cursor Tracking** – See where collaborators are typing in real time.
- **Room-based Editing** – Separate collaborative spaces for different files.
- **Modern UI** – Styled with [Tailwind CSS](https://tailwindcss.com/) and [shadcn/ui](https://ui.shadcn.com/).
- **Optimized Performance** – Built with Next.js and efficient socket event handling.

---

## Tech Stack

- **Frontend:** Next.js, TypeScript, Tailwind CSS, shadcn/ui
- **Backend:** Node.js, Express, Socket.IO
- **State Management:** Central app state
- **Styling:** Tailwind with extended theme colors
- **Linting:** ESLint with `next/core-web-vitals` rules

---

## Project Structure

```

privy-notion/
├── app/                 # Next.js app directory
├── components/          # Reusable UI components
├── server.js            # Socket.IO + Express backend server
├── tailwind.config.js   # Tailwind CSS configuration
├── postcss.config.mjs   # PostCSS setup
├── next.config.mjs      # Next.js config
└── todo.txt             # Pending tasks

````

---

## Getting Started

### 1️. Clone the Repository
```bash
git clone https://github.com/yourusername/privy-notion.git
cd privy-notion
````

### 2️. Install Dependencies

```bash
npm install
# or
yarn install
# or
pnpm install
```

### 3️. Start the Socket.IO Server

In a separate terminal:

```bash
node server.js
```

The server will run on **[http://localhost:4000](http://localhost:4000)**.

### 4️. Start the Next.js Development Server

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open **[http://localhost:3000](http://localhost:3000)** in your browser.

---

## Environment Variables

Make sure to set up any required environment variables in a `.env` file.

---

## DEV Notes

* This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to optimize Google Fonts.
* Tailwind CSS is configured with custom color palettes and animations in `tailwind.config.js`.
* The backend (`server.js`) manages:

  * Room creation and joining
  * Broadcasting changes to all clients in a room
  * Cursor movement synchronization
  * User join/leave events

---

## Deployment

The easiest way to deploy your Next.js app is via [Vercel](https://vercel.com/).

---

## License

This project is licensed under the MIT License.

