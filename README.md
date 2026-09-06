# ARC Engine Router

A lightweight, mobile-first **USDC interface for Arc Testnet**.

## What is live

- Arc Testnet wallet connection through an injected EVM provider
- Automatic Arc Testnet network switch/add flow
- Unified USDC balance display
- Native USDC transfer flow with wallet signing
- Receive address + ArcScan link
- Read-only address/contract balance lookup
- Session transaction history with ArcScan links
- Mobile-first ARC Engine branding using the repository logo

## Arc Testnet configuration

| Parameter | Value |
|---|---|
| Network | Arc Testnet |
| Chain ID | `5042002` |
| RPC | `https://rpc.testnet.arc.network` |
| Currency / gas | USDC |
| USDC ERC-20 view | `0x3600000000000000000000000000000000000000` |
| Explorer | `https://testnet.arcscan.app` |
| Faucet | `https://faucet.circle.com` |

Arc documents USDC as the native gas currency. The ERC-20 interface above is the same native USDC balance exposed through the token contract view; it is not a second balance.

## Safety decisions

This repository intentionally does **not** request seed phrases or private keys. It does not make Circle API calls, so normal wallet balance/transfer usage does not consume Circle API quota.

Swap and bridge buttons from the earlier prototype have been changed to a non-executing status section. They will only be connected after a verified integration, route, contract addresses and security checks are available.

## Stack

- HTML5 / CSS / JavaScript
- ethers.js 5.7
- Browser EVM wallet APIs
- Static deployment compatible with Vercel or any static web server

## Run locally

```bash
python -m http.server 8080
```

Then open `http://localhost:8080`.

## Builder

**AMRISH KUMAR DWIVEDI** — Web3 Developer & Arc Network Builder.

- GitHub: https://github.com/AMRISHKUMARDWIVEDI08
- Repository: https://github.com/AMRISHKUMARDWIVEDI08/arc-engine-router

## Disclaimer

This is a builder/testnet interface. Verify the recipient, network and amount in your wallet before signing. Testnet assets have no intended mainnet value.
