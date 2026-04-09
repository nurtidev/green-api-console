# GREEN-API Console

A clean, single-page web console for interacting with the [GREEN-API](https://green-api.com) WhatsApp gateway.

Built as a test assignment for the **Middle+ Backend Developer (Go)** position at GREEN-API.

## Live Demo

[https://green-api-console-production.up.railway.app](https://green-api-console-production.up.railway.app)

## Features

- **getSettings** — fetch instance configuration
- **getStateInstance** — check WhatsApp connection status
- **sendMessage** — send a text message to any WhatsApp number
- **sendFileByUrl** — send a file (image, document, etc.) via URL
- Credentials are **persisted in localStorage** — no need to re-enter on refresh
- JSON response viewer with one-click **Copy** button

## Getting Started

### 1. Create a GREEN-API instance

1. Sign up at [green-api.com](https://green-api.com) (free developer account)
2. Create a new instance
3. Scan the QR code to connect your WhatsApp number
4. Copy your `idInstance` and `ApiTokenInstance` from the dashboard

### 2. Use the console

1. Open the page
2. Enter your `idInstance` and `API Token Instance`
3. Click any method button and see the response on the right

## Running locally

No build step needed — it's a single HTML file.

```bash
git clone https://github.com/nurtidev/green-api-console.git
cd green-api-console
open index.html
```

Or with a local server:

```bash
npx serve .
```

## Deploying to Railway

```bash
# Install Railway CLI
npm install -g @railway/cli

railway login
railway init
railway up
```

Or connect the GitHub repo directly from the [Railway dashboard](https://railway.app).

## API Reference

| Method | Type | Endpoint |
|---|---|---|
| `getSettings` | GET | `/waInstance{id}/getSettings/{token}` |
| `getStateInstance` | GET | `/waInstance{id}/getStateInstance/{token}` |
| `sendMessage` | POST | `/waInstance{id}/sendMessage/{token}` |
| `sendFileByUrl` | POST | `/waInstance{id}/sendFileByUrl/{token}` |

Full docs: [green-api.com/docs](https://green-api.com/docs)

## Author

**Nurtilek Assankhan** — Middle+ Backend Developer (Go)

- Telegram: [@nurtilek_assankhan](https://t.me/nurtilek_assankhan)
- GitHub: [nurtidev](https://github.com/nurtidev)
- Location: Astana, Kazakhstan
