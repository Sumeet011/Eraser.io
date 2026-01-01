
# ✏️ Erasor.io Clone

![Build   Deploy Erasor io Clone Using Next Js   React with Typescript]

> 🚀 A full-featured collaborative whiteboard and document editor built with modern web technologies

## ✨ Features

- 📝 **Rich Text Editor** - Create and edit documents with EditorJS
- 🎨 **Collaborative Whiteboard** - Draw and collaborate using Excalidraw
- 🔐 **Secure Authentication** - User authentication powered by Kinde
- 💾 **Real-time Database** - Convex backend for instant data synchronization
- 👥 **Team Collaboration** - Work together with your team in shared workspaces
- 🌓 **Dark Mode Support** - Built-in theme switching
- 📱 **Responsive Design** - Works seamlessly on all devices

## 🛠️ Tech Stack

- **Framework**: Next.js 14 with TypeScript
- **Styling**: Tailwind CSS + Radix UI
- **Editor**: EditorJS with plugins
- **Whiteboard**: Excalidraw
- **Authentication**: Kinde Auth
- **Database**: Convex (Real-time backend)
- **Icons**: Lucide React
- **Notifications**: Sonner

## 📦 Installation

1️⃣ **Clone the repository**
```bash
git clone <repository-url>
cd erasor_clone
```

2️⃣ **Install dependencies**
```bash
npm install
# or
yarn install
# or
pnpm install
```

3️⃣ **Set up environment variables**

Create a `.env.local` file in the root directory:
```env
# Kinde Authentication
KINDE_CLIENT_ID=your_kinde_client_id
KINDE_CLIENT_SECRET=your_kinde_client_secret
KINDE_ISSUER_URL=your_kinde_issuer_url
KINDE_SITE_URL=http://localhost:3000
KINDE_POST_LOGOUT_REDIRECT_URL=http://localhost:3000
KINDE_POST_LOGIN_REDIRECT_URL=http://localhost:3000/dashboard

# Convex Database
NEXT_PUBLIC_CONVEX_URL=your_convex_url
```

4️⃣ **Run the development server**
```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

5️⃣ **Open your browser**

Navigate to [http://localhost:3000](http://localhost:3000) to see the application.

## 📁 Project Structure

```
erasor_clone/
├── app/
│   ├── (routes)/
│   │   ├── dashboard/       # Dashboard pages & components
│   │   ├── teams/           # Team management
│   │   └── workspace/       # Workspace editor & canvas
│   ├── api/
│   │   └── auth/           # Kinde authentication routes
│   ├── _components/         # Shared components
│   ├── _constant/           # Constants
│   └── _context/            # React contexts
├── components/
│   └── ui/                 # UI components (shadcn/ui)
├── convex/                 # Convex backend functions
│   ├── files.tsx           # File operations
│   ├── teams.tsx           # Team operations
│   └── user.tsx            # User operations
├── lib/                    # Utility functions
└── public/                 # Static assets
```

## 🔑 Authentication & Data Storage

### 🔐 User Authentication
- **Provider**: [Kinde Auth](https://kinde.com/)
- **Auth Route**: `/api/auth/[kindeAuth]`
- Handles login, logout, and session management

### 💾 User Data Storage
User authentication data is stored in **Convex** (real-time backend database):

**Storage Location**: Convex Database → `user` table

**User Schema**:
```typescript
{
  name: string,    // User's full name
  email: string,   // User's email (unique identifier)
  image: string    // User's profile picture URL
}
```

**Key Operations**:
- `getUser`: Query user by email
- `createUser`: Create new user record

> 📍 All user data is stored in Convex's cloud database, not locally. This enables real-time synchronization across devices and team collaboration.

## 🚀 Available Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start development server |
| `npm run build` | Build for production |
| `npm run start` | Start production server |
| `npm run lint` | Run ESLint |

## 📚 Learn More

### Next.js Resources
- 📖 [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API
- 🎓 [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial
- 💻 [Next.js GitHub](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

### Additional Resources
- 🔐 [Kinde Auth Documentation](https://kinde.com/docs/)
- 💾 [Convex Documentation](https://docs.convex.dev/)
- ✏️ [EditorJS Documentation](https://editorjs.io/)
- 🎨 [Excalidraw Documentation](https://docs.excalidraw.com/)

## 🌐 Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out the [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.

## 📄 License

This project is open source and available under the MIT License.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

---

Made with ❤️ using Next.js and Convex
