# Jay Deaton

**Senior full-stack engineer: TypeScript, React, React Native / Expo, Node.js.** 10+ years building and running the software behind a production buy-sell-trade commerce business.

**Open to senior full-stack roles (remote, hybrid, or on-site) and freelance work.** Based in Lincoln, NE.

[jaydeaton.com](https://jaydeaton.com) · [LinkedIn](https://linkedin.com/in/jay-deaton) · [jayrdeaton@gmail.com](mailto:jayrdeaton@gmail.com) · [npm (55+ packages)](https://www.npmjs.com/~jayrdeaton) · [infinitetoken.com](https://www.infinitetoken.com)

---

## Professional work

Full-stack engineer and co-founder at [Infinite Token](https://github.com/infinitetoken) since 2016. Most of that code is private, so here's the summary:

- Core engineer on a 3-6 person team building our commerce platform: 6 apps including POS, inventory, and data sync, plus a central API and databases serving 3 retail locations, 25 staff, and tens of thousands of customers
- Solo-built and launched [Lumber](https://lumber.infinitetoken.com), an end-to-end encrypted logging service for iPhone, iPad, Mac, Windows, and Linux (Android coming), with SDKs for several languages and an MCP CLI for AI agents
- Solo-built and launched [SlingScan](https://slingscan.infinitetoken.com), which turns an iPhone into a wireless barcode scanner for Mac, Windows, and Linux over local Wi-Fi with no server, built with Expo and Electron
- Built RESTful APIs and auth in Node.js/Express, plus business apps in React, React Native, and Electron
- Integrated Shopify, eBay, Google, AWS, and POS hardware and software into one system
- Implemented Stripe payments for online and in-store sales, including Stripe Terminal card readers
- Wrote native Swift modules connecting Bluetooth and Zebra label printers to React Native apps
- Planned and ran schema and data migrations on live production databases with no downtime or data loss
- Added camera-based barcode scanning for product lookup across internal tools
- Automated product-data collection with web scraping, saving hundreds of hours of manual entry
- Led the migration to TypeScript and introduced Jest unit testing and org-wide linting standards

Before that, Operations Manager at Gameroom (2013-2016), a ~30-person buy-sell-trade retailer, where I built VBA automation that cut payroll processing from 4 hours to 20 minutes and eBay inventory tooling that saved ~20 hours a week and cut listing time ~75%.

---

## Featured

### Private projects
Most of this code is private, but I'm happy to walk through the architecture.
- **[Lumber](https://lumber.infinitetoken.com)** ([App Store](https://apps.apple.com/app/id6767543372), [Microsoft Store](https://apps.microsoft.com/detail/9NCGDHB49MFR)): end-to-end encrypted cloud logging for iPhone, iPad, Mac, Windows, and Linux. SDKs for Node.js, Python, Go, PHP, and .NET encrypt each log with AES-256-GCM before it leaves the server, so the Express API, socket.io server, and workers on PostgreSQL (Supabase) only ever hold ciphertext. Each app key is wrapped per user with X25519, and new devices and teammates are confirmed with short codes over CPace. Clients: an Expo app, its Electron build for Mac, Windows, and Linux, and a CLI that hands decrypted logs to AI agents over MCP
- **[SlingScan](https://slingscan.infinitetoken.com)** ([App Store](https://apps.apple.com/app/id6832661783), [Microsoft Store](https://apps.microsoft.com/detail/9NQJK4H1NQPL)): turns an iPhone into a wireless barcode scanner for a Mac, Windows PC or Linux computer. Scans go straight to the computer over the local network, each WebSocket frame sealed with AES-256-GCM under a key shared by scanning a pairing QR code, and an Electron app types them into the app in front like a USB scanner, through macOS's CGEvent API, Windows' SendInput, X11's XTest, or Wayland's RemoteDesktop portal. The iPhone app is Expo and React Native Paper, with an offline outbox and a StoreKit 2 one-time unlock
- **CashierFu:** point-of-sale for small retailers: a Nuxt web app, native iOS and macOS apps in Swift, a WebSocket server, and an Express API with sales and inventory analytics. Each shop connects its own Stripe account to take cards on Stripe Terminal readers
- **CashierFu-Utility:** CashierFu's React Native / Expo companion app: shop staff turn products into trackable units, move and audit stock across containers, photograph units for the storefront, and print labels on Zebra Bluetooth printers through native modules. The same codebase also builds against MediaEncyclopedia's API, each backend from its own EAS profile

### `@tastic`: React Native game engine + games
Modular game-engine packages (game loop, physics, input, HUD, sprites, grid, cards, profiles, achievements, split-screen pass-and-play, and the app shell around them) that power my Expo games. DuelTastic, PuckTastic (BoxHockey until 2.0) and Swirlio are the first on the App Store, with more games and Google Play on the way. Play the web versions at [games.infinitetoken.com](https://games.infinitetoken.com).
- [React-Native-Game-Core](https://github.com/jayrdeaton/React-Native-Game-Core) (`@tastic/core`): frame-rate-independent game loop, vector math, orientation handling, background pause
- [CardTastic](https://github.com/jayrdeaton/CardTastic) ([play](https://games.infinitetoken.com/cardtastic/)): ad-free, offline collection of 20 card games (11 solitaire, 9 for two to four players with CPU opponents) for iOS, Android, and web on a shared TypeScript card engine. Its solitaire rules are `@tastic/cardtastic-engine`, shared with the game server, which replays each daily leaderboard run to check it
- [DuelTastic](https://github.com/jayrdeaton/DuelTastic) ([play](https://games.infinitetoken.com/dueltastic/), [App Store](https://apps.apple.com/app/id6834025841)): four duel games in one app (Trap, Turf, Tag and Snake) on the shared game shell, head to head on one phone or against flood-fill and distance-field CPUs
- [Hangman](https://github.com/jayrdeaton/Hangman) ([play](https://games.infinitetoken.com/hangman/))
- [HexFleet](https://games.infinitetoken.com/hexfleet/): turn-based starship battles on a hex grid, drawn in Skia, where every commander plans in secret and the whole turn plays out at once, against CPUs, by pass and play, or with friends online through an Express and Socket.IO game server. Its rules are `@tastic/hexfleet-engine`, so the app and the game server run exactly the same game
- [PuckTastic](https://github.com/jayrdeaton/PuckTastic) ([play](https://games.infinitetoken.com/pucktastic/), [App Store](https://apps.apple.com/app/id6824717751)): four tabletop puck games in one app (Box Hockey, Air Hockey, Paddles and Breaker) on one physics engine, with sub-stepped puck physics and CPUs that predict the puck or pick shots by simulating them
- [Swirlio](https://github.com/jayrdeaton/Swirlio) ([play](https://swirlio.infinitetoken.com), [App Store](https://apps.apple.com/app/id6824430243)): kaleidoscope toy drawn in Skia with up to 12 mirrored copies, 150 colliding beads simulated on the UI thread, and a mic-driven audio-reactive mode

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
| [`@rific/core`](https://github.com/jayrdeaton/React-Native-Core) | Settings Context and Redux slice factories shared by the other packages |
| [`@rific/auto-paper`](https://github.com/jayrdeaton/React-Native-Auto-Paper) | Adaptive triadic theming for react-native-paper |
| [`@rific/drawer`](https://github.com/jayrdeaton/React-Native-Drawer) | Spring-animated drawers and sheets that slide in from any screen edge |
| [`@rific/feedback-press`](https://github.com/jayrdeaton/React-Native-Feedback-Press) | Haptic pressables |
| [`@rific/focus-chain`](https://github.com/jayrdeaton/React-Focus-Chain) | Auto-incrementing focus chain hook for form inputs |
| [`@rific/gestures`](https://github.com/jayrdeaton/React-Native-Gestures) | Swipe-to-dismiss with flicks, and pinch-to-zoom about the fingers, measured in the view's own coordinates |
| [`@rific/heatmap`](https://github.com/jayrdeaton/React-Native-Heatmap) | GitHub-style activity heatmap |
| [`@rific/resizable-input`](https://github.com/jayrdeaton/React-Native-Resizable-Input) | Resizable multiline input |
| [`@rific/scanner`](https://github.com/jayrdeaton/React-Native-Scanner) | Camera barcode scanner with customizable overlays |
| [`@rific/scroll-view`](https://github.com/jayrdeaton/React-Native-Scroll-View) | ScrollView, FlatList, and SectionList with blurred floating headers and pull-to-search |
| [`@rific/splash-gate`](https://github.com/jayrdeaton/Expo-Splash-Gate) | Holds the splash screen until named async conditions are ready |
| [`@rific/sync`](https://github.com/jayrdeaton/Expo-Sync) | SQLite sync engine for Expo: schema management, upserts, deletions, cursor tracking |
| [`@rific/timer`](https://github.com/jayrdeaton/React-Native-Timer) | Animated timer ring |
| [`@rific/toaster`](https://github.com/jayrdeaton/React-Native-Toaster) | Animated toast notifications |
| [`@rific/updater`](https://github.com/jayrdeaton/Expo-Updater) | OTA update hook for Expo plus the build and update release CLI |
| [Expo-Starter](https://github.com/jayrdeaton/Expo-Starter) | Production-ready Expo starter with Redux, Paper theming, OTA updates, and `@rific` pre-wired |

**`@tastic`: React Native game engine**

| Package | Description |
|---------|-------------|
| [`@tastic/core`](https://github.com/jayrdeaton/React-Native-Game-Core) | Vec2 math, frame-clamped game loop, orientation handling, background pause |
| [`@tastic/achievements`](https://github.com/jayrdeaton/React-Native-Game-Achievements) | Headless achievement and stats engine: tiers, per-profile unlocks, streaks |
| [`@tastic/cards`](https://github.com/jayrdeaton/React-Native-Cards) | Playing-card rendering: faces, backs, court figures, suit pips |
| [`@tastic/edge-guard`](https://github.com/jayrdeaton/React-Native-Edge-Guard) | Config plugin and hook that keep iOS edge swipes from firing over game controls |
| [`@tastic/grid`](https://github.com/jayrdeaton/React-Native-Game-Grid) | Grid math for tile games: bounds, cell/pixel conversion, adjacency, BFS reachability |
| [`@tastic/hud`](https://github.com/jayrdeaton/React-Native-Hud) | Non-modal UI kit for local multiplayer: popovers, pickers, gauges, and dialogs per player zone |
| [`@tastic/input`](https://github.com/jayrdeaton/React-Native-Game-Input) | Worklet-safe input: swipe and keyboard direction, drag aiming, flick velocity |
| [`@tastic/physics`](https://github.com/jayrdeaton/React-Native-Game-Physics) | 2D arcade physics: circle and rect collisions, bounces, friction, gravity wells, springs |
| [`@tastic/profile`](https://github.com/jayrdeaton/React-Native-Game-Profile) | Per-seat player profiles with picker and roster screens |
| [`@tastic/shell`](https://github.com/jayrdeaton/React-Native-Game-Shell) | The app around a pack of games: Home, loadouts, stats, profiles, settings, and one persisted Redux store, driven by a single pack definition |
| [`@tastic/split-screen`](https://github.com/jayrdeaton/React-Native-Split-Screen) | Face-to-face or side-by-side two-player layouts based on how the device is held |
| [`@tastic/sprites`](https://github.com/jayrdeaton/React-Native-Sprites) | Shared Skia and SVG effects: fireworks, gravity wells, pucks, rink markings |

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

- **Languages:** TypeScript, JavaScript, Swift, Python, SQL, HTML/CSS, VBA
- **Frameworks:** React, Next.js, React Native, Expo, Node.js/Express, Electron, Vue/Nuxt
- **Platforms:** iOS, Android, macOS, Windows, Linux, Expo EAS, Xcode
- **Cloud & Data:** AWS (Lambda, S3, Elastic Beanstalk, ECR), Supabase, Firebase, PostgreSQL, MongoDB, Redis, SQLite, Docker, GitHub Actions, Vercel, Heroku
- **Tools & Integrations:** Git, Jest, REST, GraphQL, WebSocket, Bluetooth, Shopify, eBay, Google APIs (Gmail, Gemini, Merchant Center, Ads), Stripe, POS hardware

---

## Off the clock

Arduino projects, [Fusion 360 macros](https://github.com/jayrdeaton/Fusion360Macros), 3D printing, and 6502 assembly games ([Snake](https://github.com/jayrdeaton/6502-Snake), [LightCycles](https://github.com/jayrdeaton/6502-LightCycles)), playable in the browser at [games.infinitetoken.com](https://games.infinitetoken.com/#6502).
