# ⚡ SKS Secure Chat

A lightweight, privacy-focused real-time chat application with end-to-end encryption using OpenPGP. Built by [Sushanta Kumar Sahoo](https://github.com/SushantaKumarSahoo).

## Features

- **End-to-End Encryption** — OpenPGP.js encrypts all messages in the browser
- **Zero-Knowledge Server** — Server never sees message content or private keys
- **Real-Time Messaging** — Instant delivery via WebSocket
- **Friend Request System** — Secure key exchange between trusted contacts
- **No Registration** — Session-based 6-character user IDs
- **Cross-Platform** — Works in any modern browser
- **Self-Hosted** — Full control over your infrastructure

## Quick Start

```bash
pip install aiohttp aiohttp-cors
python server.py
```

Open `index.html` in a browser, connect to `ws://127.0.0.1:8765/ws`, upload your PGP keys, and start chatting.

## Deployment (Render)

This project is Render-ready. Push to GitHub and create a Web Service:

- **Build Command**: `pip install -r requirements.txt`
- **Start Command**: `python server.py`

## PGP Key Generation

```bash
gpg --full-generate-key
gpg --armor --export YOUR_KEY_ID > public_key.asc
gpg --armor --export-secret-keys YOUR_KEY_ID > private_key.asc
```

Upload both `.asc` files via the sidebar.
