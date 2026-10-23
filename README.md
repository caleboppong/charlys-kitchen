# Charly's Kitchen — WhatsApp Food Ordering Website

A complete responsive Vite + React food ordering website. **No database, Supabase, login, backend, or paid API is required.**

## Run on Windows (PowerShell)

1. Extract this ZIP into a new folder.
2. Open the folder in VS Code.
3. Open a terminal and run:

```powershell
npm install
npm run dev
```

4. Open the local URL printed by Vite (normally http://localhost:5173).
5. To check the production build:

```powershell
npm run build
npm run preview
```

## How orders work

Customers browse the menu, add items to a basket, choose collection or delivery, and click **Send order on WhatsApp**. The site opens WhatsApp with an itemised message addressed to **+39 320 462 3896**. The customer must press Send; the kitchen must confirm the order. The site does **not** automatically process payments, send messages, or guarantee fulfilment.

The basket is stored in the customer's browser via localStorage, not in a server database.

## Before going live

- Confirm all menu dish names and descriptions with the owner (some descriptions are provisional interpretations of the supplied photos).
- Set actual menu prices in `src/menu.js` by replacing `price:null` with numbers, or leave `null` to request a quote on WhatsApp.
- If using another currency, change `CURRENCY` and `money()` in `src/App.jsx`.
- Confirm whether delivery is offered, service area, opening hours, allergens, and food availability.
- Test the WhatsApp order flow on mobile and desktop.
- Verify the owner has permission to use all uploaded photos and promotional artwork.

## Editing content

- `src/menu.js`: names, images, prices, descriptions, availability and categories.
- `src/App.jsx`: business copy, WhatsApp number and page sections.
- `src/styles.css`: all responsive styles and colours.
- `public/images`: supplied food photos and promotional poster.
- `public/kitchen-video.mp4`: supplied promotional video.

## Deploy

This is a static Vite site suitable for Vercel or Netlify. Build command: `npm run build`. Output folder: `dist`. No environment variables needed.

## Notes

This project was made as a **separate clean project** based on the user's React/Vite sample architecture. It does not modify the original DJ Joesika project and deliberately excludes its Supabase integration and credentials.

## Charly's Kitchen app icon
The browser favicon, iPhone home-screen icon and Android web app icons now use the Charly's Kitchen branded chef logo. Files are in `public/`: `favicon.png`, `apple-touch-icon.png`, `icon-192.png`, `icon-512.png`, and `manifest.webmanifest`. For installation, deploy the website over HTTPS and use your browser's Add to Home Screen option. This project does not include an offline service worker.
