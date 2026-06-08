# Esports Prize Pool Manager (EPPM)

Secure, transparent, and instant tournament payouts powered by Stellar Soroban.

## Problem
Esports prize pools are often disputed or delayed. Organizers may fail to pay out winners on time, and players lack a transparent way to verify that prize funds are actually secured. In the Philippines, where grassroots esports tournaments are booming, the lack of a formal escrow system often leads to trust issues between organizers and teams.

## How It Works
1. **Organizer Setup:** The tournament organizer deposits the prize pool (USDC) into a secure Soroban smart contract.
2. **Winner Verification:** Once the tournament ends, the organizer updates the contract with the verified winners and their respective prize amounts.
3. **Player Claim:** Players connect their **Freighter Wallet** to verify their identity. If they are in the winners' list, they can instantly claim their reward from the contract.
4. **Community Boost:** Fans and supporters can contribute extra XLM to a "Booster" contract to increase the total prize pool for the event.

## How It Uses Stellar
- **Soroban Smart Contracts:** The core logic for escrowing prize funds and managing winner distributions is handled on-chain for 100% transparency.
- **USDC (Classic Asset):** Prizes are distributed in USDC to provide players with stable value, avoiding the volatility of other assets.
- **Trustlines:** The system ensures players have a USDC trustline before allowing a claim, preventing failed transactions.
- **Freighter API:** Used for secure identity verification and multi-signature authorization of payout claims.
- **Why Stellar?** Stellar's low transaction fees (less than $0.01) and fast 5-second finality make it the perfect platform for high-frequency esports payouts where every second counts.

## Track
StellarX Philippines Workshop @ PUP QC

## Tech Stack
- Framework: Next.js (TypeScript)
- Stellar SDK: @stellar/stellar-sdk ^15.1.0
- Wallet API: @stellar/freighter-api ^6.0.1
- Network: Testnet
- Styling: TailwindCSS (Pro Tournament Sleek Dark Theme)

## Setup & Run
To run this project locally, follow these steps:

```bash
# Clone the repository
git clone https://github.com/Binchent/Esports-Prize-Pool-Manager-EPPM-.git
cd "Project 1"

# Install dependencies
cd web
npm install

# Deploy Smart Contracts (PowerShell)
# This will set your NEXT_PUBLIC_CONTRACT_ID and NEXT_PUBLIC_PRIZE_POOL_ID
cd ..
.\scripts\deploy-prize-pool.ps1
.\scripts\deploy.ps1

# Start the development server
cd web
npm run dev
```

## Network Details
- **Network:** Testnet
- **RPC URL:** https://soroban-testnet.stellar.org
- **Passphrase:** Test SDF Network ; September 2015
- **Contract IDs:** Defined in `web/.env.local` after running deployment scripts.

## Team
- Vincent Adolf L. Sablay — @Binchent

## License
MIT
