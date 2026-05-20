<div align="center">

  ![Logo](https://raw.githubusercontent.com/plankanban/planka/master/assets/logo.png)

  # PLANKA

  _Project mastering driven by fun_

  ![Version](https://img.shields.io/github/package-json/v/plankanban/planka?style=flat-square) [![Docker Pulls](https://img.shields.io/badge/docker_pulls-8M%2B-%23066da5?style=flat-square&color=red)](https://github.com/plankanban/planka/pkgs/container/planka) [![Contributors](https://img.shields.io/github/contributors/plankanban/planka?style=flat-square&color=blue)](https://github.com/plankanban/planka/graphs/contributors) [![Chat](https://img.shields.io/discord/1041440072953765979?style=flat-square&logo=discord&logoColor=white)](https://discord.gg/WqqYNd7Jvt)

  [Install](https://docs.planka.cloud/docs/installation/docker/production-version/) ·  [Demo](https://planka.app) · [Docs](https://docs.planka.cloud/docs/welcome/) · [API](https://plankanban.github.io/planka/swagger-ui/) · [Cloud](https://planka.app/pricing) · [Pro version](https://planka.app/pro)

  ![Demo](https://raw.githubusercontent.com/plankanban/planka/master/assets/demo.gif)

</div>

## Kengmakon Development Setup

This is a Kengmakon-branded fork. To run locally:

### Prerequisites
- Docker Desktop (with WSL2 backend on Windows)
- Git

### Quick start

```bash
git clone https://github.com/Muhammadrahimw/planka.git
cd planka
docker compose -f docker-compose-dev.yml up -d
```

First start takes ~3 minutes (npm install). Subsequent starts ~10 seconds.

- **Frontend:** http://localhost:3000
- **Backend API:** http://localhost:13370

> **Note:** Port `13370` is used instead of the upstream `1337` because Windows reserves `1337`. Adjust the host port in `docker-compose-dev.yml` if you don't have that constraint.

### Default admin

The admin account is created on first start from env vars in `docker-compose-dev.yml`:

```
DEFAULT_ADMIN_USERNAME=muhammadrahim
DEFAULT_ADMIN_PASSWORD=1234
```

**Change these in `docker-compose-dev.yml` before sharing the instance.** Login uses **username only** (email is profile-only in this fork).

### Common commands

```bash
# Stop everything (data preserved)
docker compose -f docker-compose-dev.yml down

# Restart just the backend after env changes
docker compose -f docker-compose-dev.yml up -d --force-recreate planka-server

# Follow server logs
docker compose -f docker-compose-dev.yml logs -f planka-server

# Reset the database (destructive)
docker compose -f docker-compose-dev.yml down -v
```

### Branches
- `master` — Kengmakon rebrand: logo, favicon, login UI, username-only login
- `feature/ultima-sso` — adds Ultima OIDC SSO + role mapping (requires Ultima running on the same machine)

---

## Key Features

- **Collaborative Kanban Boards:** Create projects, boards, lists, cards, and manage tasks with an intuitive drag-and-drop interface
- **Real-Time Updates:** Instant syncing across all users, no refresh needed
- **Rich Markdown Support:** Write beautifully formatted card descriptions with a powerful markdown editor
- **Flexible Notifications:** Get alerts through 100+ providers, fully customizable to your workflow
- **Seamless Authentication:** Single sign-on with OpenID Connect integration
- **Multilingual & Easy to Translate:** Full internationalization support for a global audience

## How to Deploy

PLANKA is easy to install using multiple methods - learn more in the [installation guide](https://docs.planka.cloud/docs/welcome/).

For configuration and environment settings, see the [configuration section](https://docs.planka.cloud/docs/category/configuration/).

Interested in a hosted or [Pro version](https://planka.app/pro) of PLANKA? Check out the pricing on our [website](https://planka.app/pricing).

## Notes App

A testing version of the Notes app is now available on multiple platforms:

- **iOS:** Join the [TestFlight](https://testflight.apple.com/join/5eJqTaJW) to try the app
- **Windows & Android:** Download the app [here](https://planka-notes.hillerdaniel.de)

## Contact

For any security issues, please do not create a public issue on GitHub - instead, report it privately by emailing [security@planka.group](mailto:security@planka.group).

**Note:** We do NOT offer any public support via email, please use GitHub.

**Join our community:** Get help, share ideas, or contribute on our [Discord server](https://discord.gg/WqqYNd7Jvt).

## License

PLANKA is [fair-code](https://faircode.io) distributed under the [Fair Use License](https://github.com/plankanban/planka/blob/master/LICENSES/PLANKA%20Community%20License%20EN.md) and [PLANKA Pro/Enterprise License](https://github.com/plankanban/planka/blob/master/LICENSES/PLANKA%20Commercial%20License%20EN.md).

- **Source Available:** The source code is always visible
- **Self-Hostable:** Deploy and host it anywhere
- **Extensible:** Customize with your own functionality
- **Enterprise Licenses:** Available for additional features and support

For more details, check the [License Guide](https://github.com/plankanban/planka/blob/master/LICENSES/PLANKA%20License%20Guide%20EN.md).

## Contributing

Found a bug or have a feature request? Check out our [Contributing Guide](https://github.com/plankanban/planka/blob/master/CONTRIBUTING.md) to get started.

For setting up the project locally, see the [development section](https://docs.planka.cloud/docs/category/development/).

**Thanks to all our contributors!**

[![Contributors](https://contrib.rocks/image?repo=plankanban/planka)](https://github.com/plankanban/planka/graphs/contributors)
