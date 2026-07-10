# 🤖 AudioMuse AI Plugin (Navidrome)
Repository: https://github.com/NeptuneHub/AudioMuse-AI-NV-plugin

## Description
AudioMuse-AI-NV-Plugin integrates core AudioMuse-AI features directly into Navidrome, adding sonic-similarity-based Instant Mix, Radio (artist similarity), and Artist Info, on top of an extended Sonic Similarity API (from v8) for deeper third-party client integration.

## Features
* Instant Mix based on song similarity
* Radio based on artist similarity
* Artist Info showing similar artists
* Sonic Similarity API extension (from v8)
* Compatible with Navidrome's InstantMix support (from v0.60.0)

## Compatible Frontends
* Navidrome integrated web frontend
* Substreamer
* Tempus
* Symfonium (requires enabling "Use similar tracks for Radio Mix")
* Feishin
* Wavio
* Other frontends implementing `getSimilarSongs2`/`getSimilarSongs` and `getArtistInfo`

## Installation
1. Make sure Navidrome, AudioMuse-AI-NV-plugin, and the AudioMuse-AI core container are all on their latest versions.
2. Set the following environment variables (Docker Compose example):
```yaml
environment:
  - ND_PLUGINS_ENABLED=true
  - ND_PLUGINS_AUTORELOAD=true
  - ND_AGENTS=audiomuseai,lastfm,deezer
  - ND_DEVARTISTINFOTIMETOLIVE=1s
```
3. Place `audiomuseai.ndp` in Navidrome's plugins folder (default: `/data/plugins`). Download it from the [releases page](https://github.com/NeptuneHub/AudioMuse-AI-NV-plugin/releases).
4. Restart Navidrome, go to **UI > Plugins**, enable AudioMuse-AI, and set the AudioMuse-AI API URL and other configuration parameters.
5. If authentication is enabled on AudioMuse-AI, generate an apiToken on the core container and add it to the plugin configuration.

Note: the order of `ND_AGENTS` matters — Navidrome uses the first listed agent that supports sonic similarity.

## Requirements
* A running Navidrome server (with plugin support)
* An existing AudioMuse-AI deployment (separate container)

## Related Repositories
* [AudioMuse-AI](https://github.com/NeptuneHub/AudioMuse-AI) - core application
* [AudioMuse-AI Plugin for Jellyfin](https://github.com/NeptuneHub/audiomuse-ai-plugin)
* AudioMuse-AI MusicServer - Subsonic-like server with integrated sonic features

## Compatibility
* Navidrome (Plugin System)
* Docker deployments
* Linux servers
* Self-hosted music libraries

## Open Source
✅ Yes

## Price
Free
