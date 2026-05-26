# Personal Dashboard

A clean personal start page for quick browser access to frequently used tools, services, and AI assistants.

## Live Demo

[Open the dashboard on GitHub Pages](https://theb1b0p-dot.github.io/personal-dashboard/)

## Features

- Google search bar
- Tabbed link groups, including an automatic "All" tab
- Responsive link cards with Lucide icons
- Local search across cards
- Add, edit, and delete cards from the browser UI
- Add and delete custom tabs
- Export and import settings as JSON
- Reset settings back to the default configuration
- Current date and time display
- Dark glassmorphism / Apple-style visual design

## Tech Stack

- HTML, CSS, and JavaScript in a single `index.html` file
- [Tailwind CSS CDN](https://tailwindcss.com/docs/installation/play-cdn)
- [Lucide Icons CDN](https://lucide.dev/)
- [Inter](https://fonts.google.com/specimen/Inter) from Google Fonts
- Browser `localStorage` for saved settings

## How to Use

Open `index.html` directly in a browser, or use the live GitHub Pages link above.

Use the page UI to:

- switch between tabs;
- search cards locally;
- add new tabs;
- add, edit, or delete cards;
- export your settings to a JSON file;
- import settings from a JSON file;
- reset the dashboard to the default setup.

Card links open in a new browser tab.

## Use as browser new tab

- Install `Custom New Tab URL` or `New Tab Redirect`.
- Set the new tab URL to `https://theb1b0p-dot.github.io/personal-dashboard/`.
- In Yandex Browser, install the extension from the Chrome Web Store.

## How to Edit Links Manually in `index.html`

Open `index.html` and edit the `defaultTabs` JavaScript array. Each tab contains a `title` and a `services` list:

```js
{
  title: "AI Assist",
  services: [
    { name: "ChatGPT", url: "https://chat.openai.com/", icon: "sparkles" }
  ]
}
```

Each service uses:

- `name`: card title;
- `url`: link target;
- `icon`: Lucide icon name.

After editing defaults, users who already saved settings in the browser may need to use the reset button or clear localStorage to see the new defaults.

## How to Update GitHub Pages

Commit and push changes to the branch configured for GitHub Pages, usually `main`:

```bash
git add README.md
git commit -m "Add project README"
git push origin main
```

GitHub Pages will update automatically after the push if Pages is enabled for the repository.

## localStorage and JSON Import/Export Notes

Dashboard changes made in the browser are stored locally in that browser's `localStorage`. They are not synced between devices or browsers automatically.

Use JSON export/import to move settings between browsers, back up your dashboard, or restore a previous configuration.
