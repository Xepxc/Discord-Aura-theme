# Discord Aura

A customized build of the **Discord Aura** theme for BetterDiscord/Vencord — a deep night-themed interface with a blue accent palette, extended with a set of additional visual refinements on top of the original.


[![Version](https://img.shields.io/github/v/release/Xepxc/Discord-Aura-theme?include_prereleases&color=00aaff)](https://github.com/Xepxc/Discord-Aura-theme/releases/tag/v1.0.4-beta)
![Theme](https://img.shields.io/badge/base-Discord%20Aura-blue)

## Installation

This theme requires a client mod that supports custom CSS themes. Discord does not support themes natively, so you'll need one of the following installed first.

### Step 1 — Install a client mod

Choose one:

- **[Vencord](https://vencord.dev/)** — lightweight, actively maintained, recommended for most users
  1. Download the installer from the official site
  2. Run it and select your Discord installation
  3. Restart Discord

- **[BetterDiscord](https://betterdiscord.app/)** — the original client mod, larger plugin ecosystem
  1. Download the installer from the official site
  2. Run it and follow the setup wizard
  3. Restart Discord

Either mod works with this theme. If you already have one installed, skip to Step 2.

### Step 2 — Enable theme support

- **Vencord:** open Discord Settings → Vencord → enable **QuickCSS**, or use the built-in **Themes** tab
- **BetterDiscord:** open Discord Settings → BetterDiscord → **Themes**

### Step 3 — Install the theme

1. Download `Discord-Aura.css` from this repository
2. Open your themes folder: Discord Settings → Themes (or BetterDiscord/Vencord section) → **Open Themes Folder**
3. Place `Discord-Aura.css` into that folder
4. Enable the theme in the **Local Themes** / **Themes** list
5. Fully restart Discord (`Ctrl+R` is usually sufficient, but a full restart via the tray icon is recommended after installation)

## Features

Built on top of the original Aura theme, this edition adds:

### Visual effects
- **Application-wide border glow** — a soft, colored outline framing the entire client window
- **Animated gradient** on the selected server indicator, cycling through the theme's accent colors
- **Voice speaking indicator** recolored to match the theme (avatar ring and video tile border)
- **Custom scrollbar** — slim, theme-colored, with a glow effect on hover

### Interface refinements
- Custom tooltips with a themed border and subtle glow
- Restyled context menu (right-click), including the status submenu — border, rounded corners, and hover states
- Profile widget cards ("Favorite Game", "Games I Own", etc.) — themed border and glow
- Profile editing panel — clean dark background, no border
- Call disconnect / stop screen-share buttons recolored to match the theme instead of the default red

### Indicators and icons
- Typing indicator recolored to the theme's accent
- Mute/deafen icons recolored from Discord's default blurple
- Activity status icons (game controller, screen share) in the friends list recolored from green to the theme's accent
- In-client theme version label manually updated to reflect the current build

## Color palette

```css
--main-color: #00aaff;      /* primary accent */
--hover-color: #0088cc;     /* hover state */
--online-color: #00ffe7;    /* online status */
--idle-color: #00aaff;      /* idle status */
--dnd-color: #0055ff;       /* do not disturb */
--streaming-color: #5633ff; /* streaming status */
--offline-color: #43546a;   /* offline status */
```

## Technical notes

This theme relies on a combination of:
- CSS custom property overrides (e.g. `--status-speaking`, `--icon-voice-muted`)
- Targeted selectors against Discord's current internal class hashes
- `!important` overrides where necessary to take precedence over Discord's inline styles

⚠️ Discord periodically changes its internal CSS class names during client updates. If an element stops being styled correctly, the corresponding selector will need to be identified again via DevTools (`Ctrl+Shift+I`) and updated accordingly.

## Credits

- [Xepxc](https://github.com/Xepxc) — original author of the Discord Aura theme.
