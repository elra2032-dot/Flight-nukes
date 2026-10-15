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

Pilot profiles are optional and stored in the current browser's local storage.
Enter a pilot name on the welcome screen to save credits, flight progress,
aircraft, and upgrades between visits on that browser. This is a local profile,
not a password-protected account; it does not sync between devices. Guest
progress is not saved.

After a flight, spend 45 credits on a mystery hangar box for a random aircraft
unlock or a permanent upgrade. Boxes shake open before the reward is revealed.
The hangar now has 15 aircraft, including four additional late-flight planes.

Each flight visits a different location, cycling through seven themed
landscapes with matching skies, ground colors, and landmarks.

Choose **Tank defense** on the welcome screen to drive a tank and defend the
range from incoming aircraft. Aim with the mouse, fire with **F** or the
on-screen fire button, and move with **W / A / S / D** or the arrow keys.
Aircraft kills earn credits; incoming aircraft damage the tank, and each
defense round lasts one minute. The scene uses higher-detail shadows, textured
terrain, and a more detailed player tank.

Online play supports shared flight rooms and 1v1 duels. One player hosts a
duel and shares the room code; the other joins with that code. In a duel,
cannon and missile hits reduce the opponent's hull until one pilot is shot
down. Press **R** or use the on-screen turn button to turn around and fly in
the opposite direction; cannons, missiles, the plane, and chase/cockpit views
follow the new heading.

Colliding with an obstacle triggers a plane-impact explosion and damages the
hull; hitting a building while flying low causes a fatal crash and plane
explosion. Missile targets are tracked with an on-screen crosshair and progress
ring; once locked, press **Q** to launch a homing missile at the target.
