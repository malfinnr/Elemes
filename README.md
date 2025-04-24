# 📊 Sales Dashboard – Vue + Next.js + TypeScript

Live Demo: [https://elemesalfin.vercel.app](https://elemesalfin.vercel.app)

---

## ✅ Overview

This project is a simple Sales Dashboard built using:

- **Next.js** (App Router)
- **Vue.js** (via integration with Web Components)
- **TypeScript** for type safety
- **No backend/API** – uses local `dummyData.json` file
- **Deployed on Vercel**

---

## 🎯 Features

- Displays structured data from a local JSON file
- Handles nested data (e.g., deals, clients, status)
- Responsive and user-friendly interface
- Loading and error states included
- Fully static — no API or database calls

---

## 🛠️ Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/malfinnr/Elemes.git
cd Elemes
```

### Install Dependencies

```shell
npm install
```

### Run the Development Server

```shell
npm run dev
```

This command starts a local server using the production build. You can now open http://localhost:3000 in your preferred browser to see the result.

### Project structure

```shell
/
├── components/        # UI components
├── data/              # Contains dummyData.json
├── pages/             # Next.js pages
├── public/            # Static assets
├── styles/            # CSS/Tailwind/etc.
├── types/             # TypeScript interfaces/types
├── utils/             # Helper functions
└── ...
```

## 🚀 Deployment on Vercel

This project is deployed using **[Vercel](https://vercel.com)**.

### 🔗 Live App

[https://elemesalfin.vercel.app](https://elemesalfin.vercel.app)

### 📦 How to Deploy Your Own Version

1. **Push your project to GitHub**  
   Make sure your code is committed and pushed to a public or private GitHub repository.

2. **Go to [vercel.com](https://vercel.com) and log in**  
   You can sign in with your GitHub account.

3. **Create a New Project**

   - Click **“Add New Project”**
   - Select your GitHub repo
   - Vercel will auto-detect your framework (Next.js)

4. **Configure (if needed)**

   - For most Next.js projects, default settings are fine.
   - Ensure your build command is `npm run build` and the output directory is `.next`.

5. **Deploy**

   - Click **Deploy**
   - After build completes, your site will be live on a Vercel-provided domain

6. **(Optional) Set a Custom Domain**
   - Go to the project’s settings
   - Click **“Domains”** to add a custom domain or subdomain

---

Once deployed, Vercel will automatically rebuild and redeploy your app every time you push to your GitHub repo.
