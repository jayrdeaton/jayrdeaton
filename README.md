# Jay Deaton

**Senior full-stack engineer: TypeScript, React, React Native / Expo, Node.js.** 10+ years building and running the software behind a production buy-sell-trade commerce business.

**Open to senior full-stack roles (remote, hybrid, or on-site) and freelance work.** Based in Lincoln, NE.

[jaydeaton.com](https://jaydeaton.com) · [LinkedIn](https://linkedin.com/in/jay-deaton) · [jayrdeaton@gmail.com](mailto:jayrdeaton@gmail.com) · [npm (55+ packages)](https://www.npmjs.com/~jayrdeaton) · [infinitetoken.com](https://www.infinitetoken.com)

---

## Professional work

Full-stack engineer and co-founder at [Infinite Token](https://github.com/infinitetoken) since 2016. That code is private, so here's the summary:

- Core engineer on a 3-6 person team: 6 internal apps (React, React Native, Electron), a central Node/Express API, and databases serving 3 retail locations, 25 staff, and tens of thousands of customers
- Integrated Shopify, eBay, Google, AWS, and POS hardware into one system
- Migrated hundreds of thousands of records across databases with zero data loss
- Led the move to TypeScript, plus Jest testing and org-wide linting standards
- Currently building [MediaEncyclopedia](https://mediaencyclopedia.com), a graded collectible-media storefront on Next.js and Supabase, with AI product enrichment on Gemini and Claude

---

## Featured

### Private projects
The code is private, but I'm happy to walk through the architecture.
- **[MediaEncyclopedia](https://mediaencyclopedia.com):** storefront for collectible Blu-ray, 4K, DVD, and games, with every unit graded and photographed. Next.js and Supabase, an in-house grading and cataloging tool, eBay-based pricing, AI enrichment routed between Gemini and Claude, and Stripe checkout
- **MediaEncyclopedia-Utility:** MediaEncyclopedia's React Native / Expo companion app: staff turn products into trackable units, move and audit stock across containers, photograph units for the storefront, and print labels on Zebra Bluetooth printers through native modules
- **Lumber:** end-to-end encrypted cloud logging. An HTTP API, a WebSocket server for live log streaming, background workers, and PostgreSQL on Supabase, plus a mobile and web app and SDKs for Node, Python, and Swift. Logs are encrypted before they leave the device, and all decryption and search happen on the client, so the server never sees plaintext
- **CashierFu:** point-of-sale for small retailers: a Nuxt web app, native iOS and macOS apps in Swift, a WebSocket server, and an Express API with sales and inventory analytics. Each shop connects its own Stripe account to take cards on Stripe Terminal readers
- **CashierFu-Utility:** CashierFu's companion app for shop staff, the same React Native codebase as MediaEncyclopedia-Utility built against CashierFu's own API from its own EAS profile

### `@tastic`: React Native game engine + games
Modular game-engine packages (game loop, physics, input, HUD, sprites, grid, cards, profiles, achievements, split-screen pass-and-play) that power my Expo games. BoxHockey and Swirlio are the first on the App Store, with more games and Google Play on the way. Play the web versions at [games.infinitetoken.com](https://games.infinitetoken.com).
- [React-Native-Game-Core](https://github.com/jayrdeaton/React-Native-Game-Core) (`@tastic/core`): frame-rate-independent game loop, vector math, orientation handling, background pause
- [BoxHockey](https://github.com/jayrdeaton/BoxHockey) ([play](https://games.infinitetoken.com/boxhockey/), [App Store](https://apps.apple.com/app/id6824717751)): turn-based tabletop hockey with flick, slingshot, and push shots; reaction-race face-offs; and a CPU that picks shots by simulating them through the physics engine
- [Solitaire](https://github.com/jayrdeaton/Solitaire) ([play](https://games.infinitetoken.com/solitaire/)): ad-free, offline suite of 11 solitaire games for iOS, Android, and web on a shared TypeScript card engine
- [LightCycles](https://github.com/jayrdeaton/LightCycles) ([play](https://games.infinitetoken.com/lightcycles/)) · [Snake](https://github.com/jayrdeaton/Snake) ([play](https://games.infinitetoken.com/snake/)) · [Hangman](https://github.com/jayrdeaton/Hangman) ([play](https://games.infinitetoken.com/hangman/))
- [Swirlio](https://github.com/jayrdeaton/Swirlio) ([play](https://swirlio.infinitetoken.com), [App Store](https://apps.apple.com/app/id6824430243)): kaleidoscope toy drawn in Skia with up to 12 mirrored copies, 150 colliding beads simulated on the UI thread, and a mic-driven audio-reactive mode
- In development: [AirHockey](https://github.com/jayrdeaton/AirHockey), real-time air hockey with sub-stepped puck physics, a CPU that predicts the puck's path, and two-player on one device, face to face or side by side · [Pong](https://github.com/jayrdeaton/Pong)

### Live web tools
| Project | Live | Description |
|---------|------|-------------|
| [MapFolio](https://github.com/jayrdeaton/MapFolio) | [mapfolio.infinitetoken.com](https://mapfolio.infinitetoken.com) | Interactive map builder: pins, routes, captions, print-to-PDF, and share links that encode the whole map in the URL |
| [TrimBox](https://github.com/jayrdeaton/TrimBox) | [trimbox.infinitetoken.com](https://trimbox.infinitetoken.com) | Gmail inbox cleaner: scans up to 10,000 messages, surfaces bulk senders, one-click unsubscribe and bulk archive |
| [SnaPDF-Web](https://github.com/jayrdeaton/SnaPDF-Web) | [snapdf.infinitetoken.com](https://snapdf.infinitetoken.com) | Snap ChatGPT and Claude conversations to searchable PDF or text |
| [Pixelated-Web](https://github.com/jayrdeaton/Pixelated-Web) | [pixelated.infinitetoken.com](https://pixelated.infinitetoken.com) | Browser-based image pixelation with palettes and dithering |
| [GraPDF-Web](https://github.com/jayrdeaton/GraPDF-Web) | [grapdf.infinitetoken.com](https://grapdf.infinitetoken.com) | Scrape PDFs from a webpage and merge them into one booklet |

---

## Open source

**`@rific`: Expo / React Native utilities**

| Package | Description |
|---------|-------------|
| [`@rific/updater`](https://github.com/jayrdeaton/Expo-Updater) | OTA update hook for Expo plus the build and update release CLI |
| [`@rific/sync`](https://github.com/jayrdeaton/Expo-Sync) | SQLite sync engine for Expo: schema management, upserts, deletions, cursor tracking |
| [`@rific/scanner`](https://github.com/jayrdeaton/React-Native-Scanner) | Camera barcode scanner with customizable overlays |
| [`@rific/auto-paper`](https://github.com/jayrdeaton/React-Native-Auto-Paper) | Adaptive triadic theming for react-native-paper |
| [`@rific/toaster`](https://github.com/jayrdeaton/React-Native-Toaster) | Animated toast notifications |
| [`@rific/heatmap`](https://github.com/jayrdeaton/React-Native-Heatmap) | GitHub-style activity heatmap |
| [`@rific/timer`](https://github.com/jayrdeaton/React-Native-Timer) | Animated timer ring |
| [`@rific/resizable-input`](https://github.com/jayrdeaton/React-Native-Resizable-Input) | Resizable multiline input |
| [`@rific/focus-chain`](https://github.com/jayrdeaton/React-Focus-Chain) | Auto-incrementing focus chain hook for form inputs |
| [`@rific/feedback-press`](https://github.com/jayrdeaton/React-Native-Feedback-Press) | Haptic pressables |
| [`@rific/scroll-view`](https://github.com/jayrdeaton/React-Native-Scroll-View) | ScrollView, FlatList, and SectionList with blurred floating headers and pull-to-search |
| [`@rific/drawer`](https://github.com/jayrdeaton/React-Native-Drawer) | Spring-animated drawers and sheets that slide in from any screen edge |
| [`@rific/gestures`](https://github.com/jayrdeaton/React-Native-Gestures) | Swipe-to-dismiss with flicks, and pinch-to-zoom about the fingers, measured in the view's own coordinates |
| [`@rific/splash-gate`](https://github.com/jayrdeaton/Expo-Splash-Gate) | Holds the splash screen until named async conditions are ready |
| [`@rific/core`](https://github.com/jayrdeaton/React-Native-Core) | Settings Context and Redux slice factories shared by the other packages |
| [Expo-Starter](https://github.com/jayrdeaton/Expo-Starter) | Production-ready Expo starter with Redux, Paper theming, OTA updates, and `@rific` pre-wired |

**`@tastic`: React Native game engine**

| Package | Description |
|---------|-------------|
| [`@tastic/core`](https://github.com/jayrdeaton/React-Native-Game-Core) | Vec2 math, frame-clamped game loop, orientation handling, background pause |
| [`@tastic/physics`](https://github.com/jayrdeaton/React-Native-Game-Physics) | 2D arcade physics: circle and rect collisions, bounces, friction, gravity wells, springs |
| [`@tastic/input`](https://github.com/jayrdeaton/React-Native-Game-Input) | Worklet-safe input: swipe and keyboard direction, drag aiming, flick velocity |
| [`@tastic/hud`](https://github.com/jayrdeaton/React-Native-Hud) | Non-modal UI kit for local multiplayer: popovers, pickers, gauges, and dialogs per player zone |
| [`@tastic/split-screen`](https://github.com/jayrdeaton/React-Native-Split-Screen) | Face-to-face or side-by-side two-player layouts based on how the device is held |
| [`@tastic/grid`](https://github.com/jayrdeaton/React-Native-Game-Grid) | Grid math for tile games: bounds, cell/pixel conversion, adjacency, BFS reachability |
| [`@tastic/sprites`](https://github.com/jayrdeaton/React-Native-Sprites) | Shared Skia and SVG effects: fireworks, gravity wells, pucks, rink markings |
| [`@tastic/cards`](https://github.com/jayrdeaton/React-Native-Cards) | Playing-card rendering: faces, backs, court figures, suit pips |
| [`@tastic/profile`](https://github.com/jayrdeaton/React-Native-Game-Profile) | Per-seat player profiles with picker and roster screens |
| [`@tastic/achievements`](https://github.com/jayrdeaton/React-Native-Game-Achievements) | Headless achievement and stats engine: tiers, per-profile unlocks, streaks |
| [`@tastic/edge-guard`](https://github.com/jayrdeaton/React-Native-Edge-Guard) | Config plugin and hook that keep iOS edge swipes from firing over game controls |

**Node.js / CLI**

| Package | Description |
|---------|-------------|
| [`termkit`](https://github.com/jayrdeaton/TermKit) | Fluent CLI framework: nested subcommands, middleware, type coercion |
| [`cosmetic`](https://github.com/jayrdeaton/Cosmetic) | Chainable ANSI color and style library for terminals |
| [`snapdf`](https://github.com/jayrdeaton/SnaPDF) | CLI + ESM/CJS package behind SnaPDF, handling virtual scrolling |
| [`grapdf`](https://github.com/jayrdeaton/GraPDF) | CLI + ESM/CJS package behind GraPDF |
| [`pixelated`](https://www.npmjs.com/package/pixelated) | CLI + library: 40+ retro palettes, 20+ block shapes, dithering, ANSI output |
| [`reunite`](https://github.com/jayrdeaton/Reunite) · [`deplace`](https://github.com/jayrdeaton/Deplace) | Small macOS terminal utilities |

---

## Stack

- **Languages:** TypeScript, JavaScript, Python, Swift, Ruby, HTML/CSS
- **Frameworks:** React, React Native, Expo, Node.js/Express, Electron, Vue/Nuxt
- **Data:** PostgreSQL, MongoDB, SQLite, Supabase, offline-first sync
- **Platforms:** AWS, Docker, Vercel, Heroku, GitHub Actions, npm publishing
- **Integrations:** REST, GraphQL, WebSocket, Bluetooth, Shopify, eBay, POS hardware, Google & Anthropic APIs
- **Testing:** Jest, unit and integration

---

## Off the clock

Arduino projects, [Fusion 360 macros](https://github.com/jayrdeaton/Fusion360Macros), 3D printing, and 6502 assembly games ([Snake](https://github.com/jayrdeaton/6502-Snake), [LightCycles](https://github.com/jayrdeaton/6502-LightCycles)), playable in the browser at [games.infinitetoken.com](https://games.infinitetoken.com/#6502).
