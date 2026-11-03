# Jahan Foods Digital Menu

A mobile-first digital menu for Jahan Foods, a halal Bangladeshi and Chittagonian restaurant in Lakemba, NSW. It replaces the printed menu, so customers can scan a QR code and browse on their phones. Staff can switch dishes on or off each day.

## Features

- Mobile-first menu with every item and price from the printed menu
- Sticky category tabs that highlight the section you are viewing
- Live search across dishes and categories
- Tap-to-call and Google Maps directions buttons
- Light and dark mode, following the phone's setting
- Staff admin page for daily availability (`#admin`):
  - Toggle each item on or off, or a whole section at once
  - Hide unavailable items, or show them as "Sold out"
  - Optional message banner for customers (e.g. "Kacchhi finishes by 3pm")
  - "Last updated" time on the menu

## Tech

Plain HTML, CSS and JavaScript in a single file, with no frameworks, build step or dependencies. Availability is saved in the browser's `localStorage`.

## Run locally

1. Clone the repo.
2. Open `jahan-foods-menu-local.html` with the VS Code **Live Server** extension, or just open it in a browser.
3. For the admin page, add `#admin` to the URL and enter the staff PIN.

## Configuration

At the top of the script in `jahan-foods-menu-local.html`:

```js
const ADMIN_PIN = "1234";   // change this
```

To edit dishes or prices, change the `MENU` array in the same file.

## Limitations

- `localStorage` is per browser. Changes saved by staff are not visible on customers' phones.
- The PIN is stored in the page source. It keeps casual visitors out but is not real security.

## Roadmap

- Store availability on a server (Firebase or Supabase) so changes reach all customers
- Proper staff login
- Optional daily automatic reset to "all available"
