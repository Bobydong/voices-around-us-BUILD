# Second Look

This is a copy of my team's submission for Bruin Software Engineers' Build-It-Break-It hackathon at Google Spurcegoose. My team interviewed a recruiter and tried to create a new platform for triaging candidate fit and streamlining recruiter feedback.

More details in the devpost link: https://devpost.com/software/second-look-7rp3kl

---

## Table of Contents
- [About](#about)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Running Locally](#running-locally)
- [Acknowledgements](#acknowledgements)

## About

Second Look is a lightweight platform created during the Build-It-Break-It hackathon that helps recruiters and hiring teams triage candidate fit, capture structured feedback, and keep interview notes centralized. It was built quickly to validate ideas gathered from interviewing a recruiter and to demonstrate a streamlined flow for managing candidate reviews.

## Features

- Submit and store interview notes and structured feedback
- Tagging and categorization of candidate traits
- Lightweight UI for rapid review and triage
- Export or share candidate summaries (prototype)

## Tech Stack

Primary languages and technologies used:

- **Frontend**: TypeScript, React/Vue
- **Backend**: TypeScript, JavaScript
- **Database**: PostgreSQL with PL/pgSQL stored procedures
- **Styling**: HTML / CSS

## Installation

1. Clone the repository
   ```bash
   git clone https://github.com/Bobydong/voices-around-us-BUILD.git
   ```

2. Change into the project directory
   ```bash
   cd voices-around-us-BUILD
   ```

3. Install dependencies
   ```bash
   npm install
   # or
   yarn install
   ```

4. Set up the database
   - Create a PostgreSQL database
   - Apply migrations / run SQL setup scripts in the repo (if present)

5. Configure environment variables
   - Copy `.env.example` to `.env` and edit values (DB connection, ports, API keys)

6. Start the app
   ```bash
   npm run dev
   # See package.json scripts for exact commands
   ```

## Running Locally

- **Frontend**: `npm start` (or check package.json for exact script)
- **Backend**: `npm run start:server` or equivalent
- **Database**: Ensure PostgreSQL is running and the DB connection strings are set

## Acknowledgements

- Built for Bruin Software Engineers' Build-It-Break-It hackathon at Google Spurcegoose
- Devpost project page: https://devpost.com/software/second-look-7rp3kl
- Thanks to the team and everyone who gave feedback during the hackathon
