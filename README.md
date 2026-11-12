# BaseGameBot

**A free-to-play blockchain game on Reddit, powered by Base and Cloudflare Workers.**

### Problem
Reddit lacks native, lightweight games that let users play directly in the app without installing external tools. Most blockchain games require wallets, gas fees, or complex setups—blocking casual users.

### Solution
BaseGameBot is a simple, single-page game where users play a text-based adventure (e.g., "Escape the Mine") directly in Reddit. Players interact via comments, and their progress is tracked on-chain using Base, with real-time updates via Cloudflare Workers. No wallet setup required—just comment to play.

### How It Fits This Listing
| Requirement | Feature |
|------------|--------|
| **Devpost submission: app listing, demo post, repo link** | We’ll submit a Devvit app listing, a public demo post on r/DevPostGames, and a GitHub repo with the full code. |
| **Demo video required** | A 2:30 video showing how to play the game in Reddit, comment-based interaction, and on-chain state updates. |
| **Must be a small, buildable web app or API** | Single-page React app (client) + Cloudflare Worker (server) + Base smart contract (minimal). All free-tier. |
| **Use of Base and Cloudflare Workers** | Core mechanics run on Base (transactions, state) and Cloudflare (real-time updates, API). |
| **Beginner Friendly & Gaming** | Simple text game, no complex setup. Designed for casual Reddit users. |
| **No published app needed** | App will be private on Devvit until after the hackathon. |

### Architecture
- **Frontend**: React app embedded in Reddit via Devvit (comment-based UI)
- **Backend**: Cloudflare Worker API to read/write game state to Base
- **Blockchain**: Base smart contract (Solidity) storing player state and moves
- **Data**: Game state stored on-chain; updates pushed via Cloudflare Durable Objects or Webhooks
- **Authentication**: No login—players use their Reddit username as player ID

### Try It
- **Demo Post**: [r/DevPostGames post with BaseGameBot in action] (placeholder)
- **App Listing**: [devpost.com/app/basegamebot] (placeholder)
- **Repo**: [github.com/muhammet424342/basegamebot] (placeholder)

### What Is Live vs TO BUILD
**Live Today**: None of the above. This is a new project built for this hackathon.

**TO BUILD** (smallest scope to meet requirements):
1. Base smart contract (minimal) for game state (player ID, moves, score)
2. Cloudflare Worker API to read/write game state from Base
3. React frontend (single page) that renders game state and submits moves via comment
4. Devvit app that embeds the frontend in Reddit
5. Demo post on r/DevPostGames showing gameplay
6. Video demo (2:30) showing interaction and on-chain update

### Roadmap
- Day 1: Design game logic and smart contract
- Day 2: Build Cloudflare Worker API and React frontend
- Day 3: Integrate with Devvit and test in Reddit
- Day 4: Record demo video and submit

### Honest Limitations
- No user accounts or login system—uses Reddit username as identifier
- Game is text-based and simple—no graphics or complex mechanics
- No real-time multiplayer—each player plays independently
- No backend database—state stored only on-chain
