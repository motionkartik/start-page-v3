# ☕ startpage — Your Cozy New Tab Workspace

Startpage is a modern, lightweight, and highly-customizable browser start/new-tab page designed to make your browser feel personal and productive. It emphasizes clean visual design (glassmorphism, ambient glows), quick access to your favorite links, and sensible defaults that you can tweak via a built-in Settings panel.

---

## ⭐ Key Features

- **Fast, static single-page app**: No build step required — open `index.html` or serve the folder.
- **Customizable themes & color schemes**: Multiple curated color schemes (Catppuccin, Nord, Gruvbox, Tokyo Night, Dracula, Solarized, and more) with light/dark modes.
- **Personal greeting & live clock**: Displays a friendly greeting (uses your name if set) and a configurable clock (12/24h, optional seconds).
- **Configurable categories & links**: Add, edit, reorder, and hide link categories and links from the Settings UI; defaults are provided in `script.js`.
- **Search engines**: Choose or add custom search engines and search directly from the page.
- **Weather & AQI widgets**: Shows current weather and air quality (requires API keys — see Usage).
- **Footer & social links**: Tweak footer content and add social links that show in the footer.
- **Todo sidebar**: Optional floating todo lists that persist in `localStorage`.
- **Backup & restore**: Export or import all settings, categories, and links as JSON for easy migration.
- **Local persistence**: All settings, links, categories and UI state are saved to `localStorage` — no server required.

---

## Usage & Configuration

- Open the **Settings** (gear icon) to personalize the page.
- Notable settings you can change from the UI:
	- Your name (displayed in the greeting)
	- Color scheme and Light/Dark mode
	- Masonry layout toggle for links
	- Time format (12/24h) and whether to show seconds
	- Temperature unit (°F/°C) and weather location
	- Where links open (same tab, new tab, new window)
	- Enable/disable search engines, or add custom ones
	- Configure footer sections and which widgets appear

### Weather & AQI

- Weather uses OpenWeather; to enable live weather:
	1. Get an API key from https://openweathermap.org
	2. Open Settings → General → OpenWeather API Key and paste your key.
	3. Set your Weather Location (e.g., `Chicago,IL,US`).

- Air Quality Index (WAQI) can be enabled with a WAQI API key (https://aqicn.org/api/).

### Backup / Restore

- Use the **Export Settings** button in Settings to download a `.json` backup of your configuration.
- Use **Import Settings** to restore or transfer your setup to another machine.

---

## Customization for Developers

- Default categories and links are defined in `script.js` in the `defaultCategories` and `defaultLinks` variables. Edit these to change the shipped defaults.
- Search engines are defined in `allSearchEngines` inside `script.js` — you can add new engines with `id`, `name`, `url` (search prefix), and `icon` HTML.
- Icons: Font Awesome is used for icons; you can use any Font Awesome class or an emoji. See the Help tab in Settings for tips on choosing icons.

Accessibility notes:
- The app includes ARIA attributes for many interactive elements and sensible focus order for keyboard users. Please report accessibility issues or improvements.

---

## Development Notes

- The app is intentionally dependency-free (vanilla JS + CSS) and persists data in `localStorage`.
- To test changes while developing, serve the folder (see Quick Start) and open the console for log output.
- If you'd like to add a build step or package this as a browser extension, the `manifest.json` can be a starting point for converting to a web extension.

---

## Contributing

Contributions, suggestions, and fixes are welcome!

- Fork the repo, make changes, and open a pull request.
- If you're adding features, please include tests or manual steps to verify behaviour.

---

## Credits

---

## License

This project is released under the MIT License. See `LICENSE` for details.
