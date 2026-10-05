# Development environment

- This checkout is a static Persian RTL website: `index.html` and `HERO.mp4`. There is no package manager, build pipeline, backend, or database.
- Run `docker compose -f docker-compose.base44.yml up -d` to serve the bind-mounted checkout on port 3000. The Python standard-library server accepts arbitrary preview hosts. No credentials are required.
- Source edits are served directly without rebuilding. There is no browser hot-reload client; refresh the preview after edits using `reload_preview`.
- Verify with `curl -fsS http://localhost:3000/` and `curl -fsSI http://localhost:3000/HERO.mp4`; the served HTML should match `index.html`. Compose health checks confirm the HTML responds.
- Fonts and photos load from Google Fonts and Unsplash. The consultation form opens the visitor's email client via `mailto:`; it does not send email through a backend.
- No automated tests are supplied. Check the rendered page and mobile menu in a browser when one is available.
