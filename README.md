# sae-downloader

# Video Downloader (Front-end on GitHub Pages + yt-dlp-host backend)

This repo provides a static front-end (hosted on GitHub Pages) that talks to a self-hosted backend API powered by `yt-dlp` (via `yt-dlp-host`) to prepare and serve downloadable video files.

## What you get

- `index.html` — a simple, minimal UI to paste a video page URL and request the backend to fetch/prepare the file.
- `docker-compose.yml` — runs a prebuilt `yt-dlp-host` container to act as the server.

## Quick setup (local / VPS)

1. Create a new GitHub repo and enable GitHub Pages (use the `main` branch root or the `/docs` folder). Copy `index.html` to the repo root (or to `/docs`) and enable Pages.

2. On a VPS (or local machine) run the backend:

```bash
# copy docker-compose.yml and .env.example -> .env
# edit .env to set your API_KEY (or leave empty) and change DOWNLOADS_DIR if needed
docker-compose up -d
