# 🤖 AudioMuse AI Plugin (Jellyfin)
Repository: https://github.com/NeptuneHub/audiomuse-ai-plugin

## Description
AudioMuse-AI-Plugin integrates core AudioMuse-AI features directly into Jellyfin, adding scheduled analysis, clustering, and sonic fingerprint tasks, plus a 1:1 API mapping so frontend developers can call Jellyfin endpoints directly for playlist creation, similar tracks, similar artists, path-finding, text/semantic search, and more.

## Features
* Scheduled tasks: music analysis (daily), clustering (weekly), sonic fingerprint (weekly)
* Instant Mix integration on artists, albums, songs, and playlists
* AI-powered playlist creation (chat-based and by track ID)
* Similar tracks and similar artists search
* Song Alchemy (add/subtract songs or artists to build a vibe-based playlist)
* CLAP-based natural language text search
* Full 1:1 API mapping with AudioMuse-AI for custom frontend integration

## Compatible Frontends
* Jellyfin web frontend and official mobile app
* Finamp
* Jellify
* Symfonium
* Feishin
* Wavio
* Other frontends via the exposed API

## Installation
### Via Plugin Catalog
1. Go to **Jellyfin > Control Panel > Plugin Catalog**.
2. Click the gear icon to add a new manifest.
3. Add the manifest: `https://raw.githubusercontent.com/NeptuneHub/audiomuse-ai-plugin/master/manifest.json`
4. Find AudioMuse AI under the General section and install it.
5. Restart Jellyfin.
6. Configure the plugin with your AudioMuse-AI container URL (e.g. `http://192.168.3.14:8000`).

### Requirements
* A running Jellyfin server
* An existing AudioMuse-AI deployment (separate container)

## Related Repositories
* [AudioMuse-AI](https://github.com/NeptuneHub/AudioMuse-AI) - core application
* [AudioMuse-AI Helm Chart](https://github.com/NeptuneHub/AudioMuse-AI) - Kubernetes deployment

## Compatibility
* Jellyfin (Plugin System)
* Docker deployments
* Linux servers
* Self-hosted music libraries

## Open Source
✅ Yes

## Price
Free
