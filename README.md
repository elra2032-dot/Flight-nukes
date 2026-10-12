# Cloudbound — Flight Club

Cloudbound is a static browser game. The complete game source is in
`index.html`; upload that one file to any static web host, or open it in a
browser. No build step or server is needed. Three.js, PeerJS, and fonts load
from external CDNs, so gameplay needs an internet connection.

## Publish with GitHub Pages

1. Create a **public** repository on GitHub.
2. Add `index.html` and the `.github/workflows/pages.yml` file from this
   folder to the repository, keeping the same paths.
3. In the repository, open **Settings → Pages** and select **GitHub Actions**
   under **Build and deployment**.
4. Push or upload the files to the repository's `main` branch. The workflow
   will publish the game; its URL appears under **Actions** and **Settings →
   Pages** after deployment finishes.

Multiplayer also needs access to PeerJS signaling and WebRTC connections.
