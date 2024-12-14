# IBRL Agent

<div align="center">
  <img src="public/IBRL.jpeg" alt="IBRL Agent" width="400" style="border-radius: 10px; margin: 20px 0; box-shadow: 0 4px 8px rgba(0,0,0,0.1);" />

A sophisticated Solana-focused AI agent with chat interface.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Next.js](https://img.shields.io/badge/Next.js-14-black)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-blue)](https://www.typescriptlang.org/)
[![Solana](https://img.shields.io/badge/Solana-1.87-purple)](https://solana.com/)

</div>

## 🚀 Features

- **Real-time Solana Data**
  - Live price tracking and market analysis
  - Trending token insights
  - Wallet balance monitoring
  - Transaction analysis with detailed breakdowns
  - Jito MEV rewards tracking
  - Compressed NFT minting

- **AI-Powered Interactions**
  - Natural language processing via GPT-4
  - Context-aware responses
  - Blockchain-specific knowledge integration
  - Sarcastic personality traits
  - Custom function calling

- **Wallet Integration**
  - Built-in agent wallet functionality
  - Secure SOL transfers
  - Transaction validation
  - Balance management
  - NFT minting capabilities

- **Developer Experience**
  - TypeScript support
  - Hot reload development
  - Comprehensive API documentation
  - Rate limiting protection
  - Error handling with personality

- **Third-Party Integrations**
  - Helius RPC integration
  - Crossmint NFT minting
  - Jito MEV analytics
  - CoinGecko price feeds
  - Jupiter Swap
  - Birdeye API

## Prerequisites

Before you begin, ensure you have the following installed:
- Node.js 
- npm, yarn, pnpm, or bun

## Environment Setup

1. Create a `.env.local` file in the root directory
2. Add the following environment variables:
```bash
NEXT_PUBLIC_HELIUS_API_KEY=your_helius_api_key
WALLET_MNEMONIC=your_wallet_mnemonic
CROSSMINT_API_KEY=your_crossmint_api_key
NEXT_PUBLIC_QUICKNODE_RPC_URL=your_quicknode_rpc_url # optional backup for helius
NEXT_PUBLIC_BIRDEYE_API_KEY=your_birdeye_api_key
```

## Getting Started

1. Clone the repository:
```bash
git clone https://github.com/introvertmac/IBRL.git
cd IBRL
```

2. Install dependencies:
```bash
npm install
# or
yarn install
# or
pnpm install
# or
bun install
```

3. Run the development server:
```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## Project Structure

```
├── src/
│   ├── app/
│   │   ├── api/
│   │   │   └── birdeye/
│   │   │       └── trending/
│   │   │           └── route.ts
│   │   │   └── crossmint/
│   │   │       └── route.ts
│   │   │   └── wallet/
│   │   │       └── balance/
│   │   │           └── route.ts
│   │   │       └── send/
│   │   │           └── route.ts
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   └── globals.css
│   ├── components/
│   │   ├── Chat.tsx
│   │   └── ApiKeyModal.tsx
│   └── utils/
│       ├── wallet.ts
│       ├── helius.ts
│       ├── coingecko.ts
│       ├── validation.ts
│       ├── jito.ts
│       └── openai.ts
│       └── jup.ts
│       └── birdeye.ts
├── public/
│   └── assets/
├── types/
│   └── index.ts
├── next.config.js
├── tailwind.config.js
├── tsconfig.json
└── package.json
```

## API Routes

```
POST /api/crossmint
├── Mint compressed NFTs
├── Parameters:
│   ├── recipient: string
│   ├── name: string
│   ├── image: string
│   └── description: string
└── Returns: NFT minting response

GET /api/wallet/balance
├── Get wallet balance
└── Returns: Balance in SOL and USD

POST /api/wallet/send
├── Send SOL to address
├── Parameters:
│   ├── recipient: string
│   └── amount: number
└── Returns: Transaction signature

GET /api/birdeye/trending
├── Get trending tokens from Birdeye
├── Parameters:
│   ├── limit: number (default: 10)
└── Returns: List of trending tokens
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

