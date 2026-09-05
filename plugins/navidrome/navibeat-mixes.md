# 🎵 NaviBeat Mixes

NaviBeat Mixes is a Navidrome plugin that builds playlists from each user's listening habits.
It creates ordinary playlists through the Subsonic API, so they are available in the Navidrome web interface and in any compatible client without installing anything on the client side.

## ⭐ Features

- **Platform:** Navidrome 0.63.1+
- **License:** GPL-3.0-or-later
- **Open Source:** ✅ Yes
- **Price:** 🆓 Free
- **Requirements:** Navidrome plugins enabled
- **Highlights:**
  - Morning, Afternoon, Evening, and Night mixes based on listening time
  - Rediscover mix for loved music that has not been played in months
  - New Music, Loved Songs, On Repeat, Essentials, and Weekly Discovery playlists
  - Genre, Artist, Daily Mix, Decade, and Wrapped playlists
  - Up to 23 optional playlists per account
  - Playlist names remain stable while their contents rotate
  - Per-user mixes with configuration for which accounts receive them
  - No client-side installation required

## 🧠 How It Learns

Rediscover can work immediately from existing Navidrome stars and play dates.
Time-of-day mixes become more personal as the plugin observes listening activity; until enough history is available, they are built from the user's most-played music and identify that state in the playlist description.

Listening history remains on the Navidrome server by default. Optional Wrapped sharing is disabled by default and can send only aggregate statistics to `navibeat.app`.

## 📦 Installation

1. Download `navibeat-mixes.ndp` from the [latest release](https://github.com/nenadjokic/navibeat-mixes/releases/latest).
2. Place the file in the Navidrome plugins directory.
3. Enable plugins in `navidrome.toml`:

```toml
[Plugins]
Enabled = true
```

4. Restart Navidrome and enable NaviBeat Mixes in **Settings > Plugins**.

The plugin refreshes mixes daily. Its declared permissions are used to schedule refreshes, read the library, create playlists, store listening history, and handle per-user data.

## 🔗 Links

- [GitHub repository](https://github.com/nenadjokic/navibeat-mixes)
- [Website](https://navibeat.app/)
- [Latest release](https://github.com/nenadjokic/navibeat-mixes/releases/latest)
