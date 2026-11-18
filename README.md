# GDG RIT Hassan — Campus Community Website

A responsive, single-page website concept for the Google Developer Groups (GDG) on Campus chapter at Rajeev Institute of Technology (RIT), Hassan. It brings chapter information, events, student projects, a knowledge quiz, and community details together in one place.

## Features

- Chapter landing page with navigation to the main sections
- Light and dark theme toggle
- Event cards with category filters, text search, RSVP form, and a **My Tickets** view
- Student project showcase with a project submission form and like buttons
- Interactive skill quiz with answer feedback and a badge-saving option
- Chapter team, mentorship information, and expandable FAQ items
- Responsive layout for desktop and mobile screens

## Technology stack

- [React](https://react.dev/) 19
- [TypeScript](https://www.typescriptlang.org/)
- [Vite](https://vite.dev/) 6
- [Tailwind CSS](https://tailwindcss.com/) 4
- [Lucide React](https://lucide.dev/) for icons
- [Motion](https://motion.dev/) for animation support

## Requirements

- Node.js (current LTS recommended)
- npm

## Run locally

1. Clone this repository and open its folder in a terminal.
2. Install dependencies:

   ```bash
   npm install
   ```

3. Start the development server:

   ```bash
   npm run dev
   ```

4. Open the URL printed by Vite. This project configures the development server to use port `3000` (typically `http://localhost:3000`).

## Available scripts

| Command | Description |
| --- | --- |
| `npm run dev` | Start the Vite development server on port 3000. |
| `npm run build` | Build the site into the `dist/` directory. |
| `npm run preview` | Preview the production build locally. |
| `npm run lint` | Run TypeScript type checking (`tsc --noEmit`). |

## Project layout

```text
.
├── index.html
├── src/
│   ├── App.tsx                  # Page composition and shared state
│   ├── main.tsx                 # React entry point
│   ├── index.css                # Global styles
│   ├── components/              # Page sections and UI components
│   ├── data/mockData.ts         # Example events, projects, quiz, and team
│   └── types.ts                 # TypeScript data types
├── public/                      # Static public assets
├── package.json
├── tsconfig.json
└── vite.config.ts
```

## Demo content and current limitations

This repository currently works as a front-end prototype. Event, project, quiz, and team information is supplied as sample data in `src/data/mockData.ts`. RSVP tickets are stored in the browser's local storage. Project submissions and likes update the current page state and are not saved to a server. The membership form displays a confirmation but does not submit registrations to a backend.

The project includes Gemini-related packages and an `.env.example`, but the current page does not call the Gemini API. No API key is needed to run the current front-end demo. If you later add server-side Gemini functionality, keep credentials in a server-side environment file or secret manager; never commit real API keys.

## Deployment

Build the static site with:

```bash
npm run build
```

The generated files are in `dist/`. Deploy that directory to a static hosting provider such as Firebase Hosting, Cloudflare Pages, or GitHub Pages. Configure the host to serve `index.html` for the site root.

## Contributing

Contributions are welcome. Fork the repository, create a branch for your change, and open a pull request with a concise description of what you changed.

## License

No license is specified yet. Add a `LICENSE` file before redistributing this project if you want to grant others explicit reuse rights.
