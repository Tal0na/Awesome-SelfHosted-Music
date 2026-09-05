# 🐳 Watchtower

Watchtower automatically updates running Docker containers when a newer image is available.
It pulls the new image, stops the existing container, and recreates it with the same deployment options.

> ⚠️ **Maintenance status:** The official Watchtower repository was archived on December 17, 2025 and is no longer maintained. Treat it as a legacy option and review current alternatives before using it on an important server.

## ⭐ Features

- **Type:** Docker container update automation
- **License:** Apache-2.0
- **Open Source:** ✅ Yes
- **Best suited for:** Homelabs and non-critical personal services
- **Highlights:**
  - Automatically checks Docker image registries for updates
  - Recreates containers while preserving their original options
  - Supports scheduled checks and notification integrations
  - Can be limited to containers explicitly marked for updates

## 🚀 Quick Start

```yaml
services:
  watchtower:
    image: containrrr/watchtower:1.7.1
    container_name: watchtower
    restart: unless-stopped
    volumes:
      - /var/run/docker.sock:/var/run/docker.sock
    command: --schedule "0 0 4 * * *"
```

The example checks for updates daily at 04:00. Start it with:

```bash
docker compose up -d
```

## 🔐 Security Notes

- Mounting `/var/run/docker.sock` gives Watchtower broad control over the Docker daemon.
- Do not expose the Docker socket over the network.
- Pin a version instead of using `latest` when predictable updates matter.
- Test updates and keep backups of application data before enabling automation.
- The upstream project does not recommend Watchtower for commercial or production environments.

## 🔗 Links

- [Archived GitHub repository](https://github.com/containrrr/watchtower)
- [Documentation](https://containrrr.dev/watchtower)
- [Docker Hub](https://hub.docker.com/r/containrrr/watchtower)
- [Latest release](https://github.com/containrrr/watchtower/releases/latest)
