# 10x-cards

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) <!-- Placeholder - Update if license differs -->

## Table of Contents

- [1. Project Description](#1-project-description)
- [2. Tech Stack](#2-tech-stack)
- [3. Getting Started Locally](#3-getting-started-locally)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the Development Server](#running-the-development-server)
- [4. Available Scripts](#4-available-scripts)
- [5. Project Scope](#5-project-scope)
  - [In Scope (MVP)](#in-scope-mvp)
  - [Out of Scope (MVP)](#out-of-scope-mvp)
- [6. Project Status](#6-project-status)
- [7. License](#7-license)

## 1. Project Description

10x-cards aims to streamline the creation and management of educational flashcards. It leverages LLM APIs (via Openrouter.ai) to automatically generate flashcard suggestions (questions and answers) from user-provided text, significantly reducing the time and effort required compared to manual creation. This facilitates the use of effective learning methods like spaced repetition.

## 2. Tech Stack

-   **Frontend:**
    -   [Astro 5](https://astro.build/): High-performance web framework.
    -   [React 19](https://react.dev/): UI library for interactive components.
    -   [TypeScript 5](https://www.typescriptlang.org/): Static typing for JavaScript.
    -   [Tailwind CSS 4](https://tailwindcss.com/): Utility-first CSS framework.
    -   [shadcn/ui](https://ui.shadcn.com/): Re-usable UI components built with Radix UI and Tailwind CSS.
-   **Backend (BaaS):**
    -   [Supabase](https://supabase.com/): Open-source Firebase alternative.
        -   PostgreSQL Database
        -   Authentication
        -   SDKs for backend interactions
-   **AI Integration:**
    -   [Openrouter.ai](https://openrouter.ai/): API access to various LLMs (OpenAI, Anthropic, Google, etc.) for flashcard generation.
-   **CI/CD & Hosting:**
    -   [GitHub Actions](https://github.com/features/actions): Continuous Integration and Deployment pipelines.
    -   [DigitalOcean](https://www.digitalocean.com/): Hosting via Docker container (planned).

## 3. Getting Started Locally

Follow these instructions to set up the project environment on your local machine.

### Prerequisites

-   **Node.js:** Version `22.14.0` is required. We recommend using a Node version manager like [nvm](https://github.com/nvm-sh/nvm) or [fnm](https://github.com/Schniz/fnm). If you have one installed, you can run `nvm use` or `fnm use` in the project directory to switch to the correct version specified in `.nvmrc`.
-   **Package Manager:** npm (included with Node.js), [yarn](https://yarnpkg.com/), or [pnpm](https://pnpm.io/). The examples below use `npm`.

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/ProgTom00/10x-cards.git
    cd 10x-cards
    ```

2.  **Install dependencies:**
    ```bash
    npm install
    ```

3.  **Set up environment variables:**
    Create a `.env` file in the root of the project. You will need credentials for Supabase and Openrouter.ai.
    ```dotenv
    # .env

    # Supabase credentials (replace with your actual Supabase project details)
    PUBLIC_SUPABASE_URL=YOUR_SUPABASE_URL
    PUBLIC_SUPABASE_ANON_KEY=YOUR_SUPABASE_ANON_KEY

    # Openrouter.ai API Key (replace with your actual key)
    OPENROUTER_API_KEY=YOUR_OPENROUTER_API_KEY

    # Add any other necessary environment variables here
    ```
    *Note: Obtain these keys from the respective service dashboards.*

### Running the Development Server

Once dependencies are installed and environment variables are set, you can start the development server:

```bash
npm run dev
```

This command will start the Astro development server, typically available at `http://localhost:4321`.

## 4. Available Scripts

The `package.json` file includes the following scripts:

-   `npm run dev`: Starts the Astro development server with HMR (Hot Module Replacement).
-   `npm run build`: Builds the application for production.
-   `npm run preview`: Starts a local server to preview the production build.
-   `npm run astro`: Accesses the Astro CLI for various commands.
-   `npm run lint`: Lints the codebase using ESLint.
-   `npm run lint:fix`: Lints the codebase and attempts to automatically fix issues.
-   `npm run format`: Formats the codebase using Prettier.

## 5. Project Scope

### In Scope (MVP)

-   Automatic flashcard generation from user-provided text via LLM API.
-   User review, editing, acceptance, or rejection of AI-generated suggestions.
-   Manual creation, editing, and deletion of flashcards.
-   Basic user authentication (registration, login).
-   Integration with a ready-made spaced repetition algorithm library for learning sessions.
-   Secure storage of user data and flashcards (GDPR compliant).
-   Collection of basic statistics on AI generation usage and acceptance rates.

### Out of Scope (MVP)

-   Developing a custom, advanced spaced repetition algorithm.
-   Gamification features.
-   Native mobile applications (Web only for MVP).
-   Importing flashcards from various document formats (e.g., PDF, DOCX).
-   A public API for third-party integrations.
-   Sharing flashcard sets between users.
-   Advanced notification systems.
-   Advanced keyword search for flashcards.

## 6. Project Status

This project is currently **under active development**. The version `0.0.1` indicates it is in the early stages. Features and functionality may change.

<!-- Consider adding badges here later:
[![Build Status](...)](...)
[![Version](...)](...)
-->

## 7. License

This project is licensed under the MIT License. See the `LICENSE` file for details.