# Shuja Sajid — Academic Website

Personal academic website of **Shuja Sajid**, Research Scholar in the Department of Computer Science at [Jamia Millia Islamia](https://www.jmi.ac.in/), New Delhi.

🌐 Live: <https://shujasajid.github.io>

Built with the [al-folio](https://github.com/alshedivat/al-folio) Jekyll starter (v1.x).

## Run locally

Requires [Docker](https://docs.docker.com/get-docker/) and Docker Compose.

```bash
docker compose pull
docker compose up
```

Open <http://localhost:8080>. Page edits reload automatically; restart the container after `_config.yml` edits:

```bash
docker compose restart
```

## Content map

| What                                     | Where                                        |
| ---------------------------------------- | -------------------------------------------- |
| About page + profile photo               | `_pages/about.md`, `assets/img/prof_pic.jpg` |
| CV (page render + auto-generated PDF)    | `_data/cv.yml`, design in `assets/rendercv/` |
| Publications                             | `_bibliography/papers.bib`                   |
| Projects                                 | `_projects/`                                 |
| GitHub repositories page                 | `_data/repositories.yml`                     |
| Social links                             | `_data/socials.yml`                          |
| Site settings (name, URL, feature flags) | `_config.yml`                                |

## Deployment

A push to `main` triggers two workflows:

- **Deploy site** — builds the Jekyll site and publishes it to the `gh-pages` branch, served at <https://shujasajid.github.io>.
- **Render a CV** — regenerates the CV PDF from `_data/cv.yml` into `assets/rendercv/rendercv_output/` and commits it back.

## Notes

- The navbar menu centering is a small site-owned style override (`assets/css/main.scss` + `_sass/_navbar-center.scss`), tracked in `.al-folio-overrides.yml`. See `docs/ARCHITECTURE.md` and `docs/CUSTOMIZE.md` for the override workflow.
- Upstream template docs live in `docs/` and are excluded from the built site.

## Credits

Based on [al-folio](https://github.com/alshedivat/al-folio) (MIT License). See [LICENSE](LICENSE).
