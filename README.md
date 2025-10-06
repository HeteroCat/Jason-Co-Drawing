# Co-Drawing App

A collaborative drawing assistant powered by Google Gemini, built with React and Vite. The app lets you describe an illustration idea in natural language and iteratively refine the artwork with AI-generated guidance.

## Features

- 🎨 Interactive drawing board with AI-driven suggestions
- 💡 Prompt-based idea refinement and iteration
- ⚡ Lightning-fast local development with Vite
- ☁️ Ready for one-click deployment to Vercel

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) 18 or later
- A Google Gemini API key

### Installation

```bash
npm install
```

### Environment Variables

Create a `.env.local` file at the project root with your Gemini API key:

```bash
GEMINI_API_KEY=your_api_key_here
```

### Local Development

Start the development server with hot reloading:

```bash
npm run dev
```

The Vite dev server prints the local URL (typically `http://localhost:5173`).

### Production Build

Create an optimized production build:

```bash
npm run build
```

Preview the production bundle locally:

```bash
npm run preview
```

## Deploying to Vercel

You can deploy directly from the Vercel dashboard or via the CLI.

### Option 1: Vercel Dashboard

1. Push your code to a GitHub, GitLab, or Bitbucket repository.
2. In the [Vercel dashboard](https://vercel.com/dashboard), select **Add New… → Project** and import the repository.
3. When prompted for build settings, set:
   - **Framework Preset:** `Vite`
   - **Build Command:** `npm run build`
   - **Output Directory:** `dist`
4. Add an environment variable named `GEMINI_API_KEY` with your key.
5. Click **Deploy**. Vercel will build and deploy your app automatically.

### Option 2: Vercel CLI

1. Install the CLI (one time):
   ```bash
   npm i -g vercel
   ```
2. Login and link the project:
   ```bash
   vercel login
   vercel
   ```
3. During the `vercel` command, accept the detected Vite configuration, set the build command to `npm run build`, and the output directory to `dist`.
4. Add the environment variable:
   ```bash
   vercel env add GEMINI_API_KEY
   ```
5. Deploy:
   ```bash
   vercel --prod
   ```

Vercel will handle future deployments automatically when you push to the connected Git branch.

## Project Structure

```
├── Home.tsx          # Main React component for the drawing experience
├── index.tsx         # App entry point
├── index.css         # Global styles
├── index.html        # Base HTML template used by Vite
├── vite.config.ts    # Vite configuration
└── tsconfig.json     # TypeScript configuration
```

## Troubleshooting

- Ensure `GEMINI_API_KEY` is set in both local `.env.local` and Vercel project settings.
- If the dev server fails to start, delete `node_modules` and reinstall dependencies with `npm install`.
- For additional Vite configuration options, see the [Vite documentation](https://vitejs.dev/).

## License

This project is provided as-is without an explicit license. Contact the original author for reuse permissions.
