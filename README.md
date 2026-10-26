# Canvas

A minimal developer profile directory. Each developer adds their name, GitHub handle, star count, project count, and languages, and profiles are listed by total stars.

## Features

- Create a profile with name, GitHub handle, total stars, public project count, and languages
- Profiles are listed in order of GitHub stars, highest first
- Entries are saved to a local JSON file

## Getting started

Requires Node.js.

```bash
npm install
npm start
```

Then open http://localhost:3008. `npm run dev` runs the same command.

## How it works

- `index.html` contains the profile form and the list of profiles. It calls the API at `http://localhost:3008`.
- `server.js` is an Express app that serves the page and exposes:
  - `POST /api/developers` to save a profile.
  - `GET /api/developers` to return all profiles sorted by stars.
- Data is written to `data.json`, created on first run and ignored by git.
- `utils.js` holds validation and file helpers that are not yet wired into `server.js`.

## Status

Prototype. Stars and project counts are typed in by the user; the app does not call the GitHub API, and there are no accounts or public profile pages.

## License

MIT, see [LICENSE](LICENSE).
