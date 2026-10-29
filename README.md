# NeonCraft — Minecraft hosting concept

A free, Android-friendly **static prototype** in a dark blue/neon theme. Includes a landing page, example plan page, and interactive **simulated** dashboard. No real VPS, Minecraft server, payments, authentication or backend are included.

## Preview locally on Android

Install Termux from its official F-Droid/GitHub source. In Termux:

```sh
pkg update && pkg upgrade -y
pkg install python git -y
cd /path/to/neoncraft-hosting
python -m http.server 8000
```

Open `http://localhost:8000` on your phone. Alternatively, open `index.html` in a browser (local links should work).

## Publish a demo on GitHub Pages

1. Create a GitHub repository, e.g. `neoncraft-hosting`.
2. Upload the **contents** of this folder to the repository root, including `index.html`.
3. Go to **Settings → Pages → Build and deployment**.
4. Choose **Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
5. Visit `https://YOUR-USERNAME.github.io/neoncraft-hosting/` once GitHub finishes publishing.

GitHub Pages is static hosting, **not a VPS**. It cannot run a Minecraft server, Docker, Pterodactyl, a persistent Node backend, or a real control panel. GitHub Pages is not intended for running a commercial SaaS/hosting business; this project is a non-commercial demo.

## Files
- `index.html`: landing page
- `pricing.html`: illustrative future tiers, no real pricing or checkout
- `dashboard.html`: simulated server controls and console
- `style.css`: responsive dark blue/neon design
- `script.js`: demo interactions, no network calls

## Future production checklist

- Obtain a suitable VPS or dedicated host with an eligible account and adequate resources.
- Follow official Pterodactyl Panel + Wings installation docs, or use another maintained panel.
- Set up a backend, secure authentication, HTTPS, firewall, monitoring and backups.
- Store secrets server-side, never in public GitHub or frontend JavaScript.
- Integrate backend APIs securely; do not expose Pterodactyl application API keys to browsers.
- Validate server capacity, terms, legal/payment requirements and support processes before any public launch.

This is an independent concept and is not affiliated with Mojang or Microsoft.
