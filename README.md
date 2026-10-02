# Track – scooter tracking, pay-per-minute rides, and an endless-runner mini-game

Open `index.html` in a browser (or `npx http-server .`). No build step, no dependencies.

- **Map**: live city map with scooters (green = free, red = in use, yellow = yours). Tap one to unlock.
- **Billing**: $0.35 per started minute, charged at unlock and at each new minute; the ride locks automatically if the balance runs out.
- **Ride**: Subway-Surfers-style runner – ←/→ change lane, ↑ jump (or swipe). 25 coins = 1 free minute.
- **Wallet / History**: save a card (Luhn-checked, only last 4 digits kept), add funds, view past rides.

Test tip: `index.html?speed=30` makes ride time run 30× faster.

## Demo limits
Payments and scooter positions are simulated and stored in `localStorage`. For real use, charge
through a processor (e.g. Stripe) from a server, and read scooter GPS from your IoT backend.
