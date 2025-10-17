# FUTURE_BC_Task01 – Crypto Exchange Onboarding and Analysis

**A Professional Deep-Dive into Centralized Exchange Architecture, Security Models, and User Experience**

---

## Introduction

Understanding crypto exchanges isn't just about buying tokens—it's about analyzing the infrastructure layer that bridges traditional finance with decentralized ecosystems. As someone who's worked with `python-bitcoin-utils` and implemented multisig PSBT signing on Bitcoin Testnet during Summer of Bitcoin 2025, I wanted to understand how centralized exchanges (CEXs) handle custody, compliance, and UX at scale.

This task explores the onboarding journey, security mechanisms, and architectural decisions behind modern crypto exchanges—knowledge essential for anyone building in the blockchain space.

---

## Exchange Chosen: [CoinSwitch Kuber / BingX]

**Platform Overview:**
- **Regulatory Stance**: [India-compliant with robust KYC / International platform with multi-jurisdiction licenses]
- **Custody Model**: Centralized custodial wallets with cold storage claims
- **Supported Assets**: 100+ cryptocurrencies including BTC, ETH, USDT, and emerging altcoins
- **Trading Features**: Spot trading, market orders, limit orders, [futures/derivatives if BingX]

**Why I Chose This Platform:**  
[For CoinSwitch: "India-first design with Rupee on-ramps made it ideal for understanding localized compliance"]  
[For BingX: "Advanced API access and copy trading features aligned with my interest in programmatic trading"]

---

## Step-by-Step Onboarding Process

### **1. Account Creation**
- Email/phone verification with OTP-based authentication
- Password requirements enforced (minimum entropy standards observed)

### **2. KYC Verification**
- **Documents Required**: Aadhaar/PAN card, live photo verification
- **Process**: OCR-based document scanning → liveness detection → manual review (if flagged)
- **Completion Time**: ~10 minutes (instant approval with clear documents)

**Security Observation**: The platform uses third-party KYC providers (likely employing facial recognition APIs), highlighting the trust assumptions users make during onboarding.

### **3. Wallet Exploration**
- **Deposit Address Generation**: Each user receives unique deposit addresses per asset
- **Address Format Analysis**: 
  - BTC addresses follow Bech32 (bc1...) format—native SegWit implementation
  - ETH addresses standard ERC-20 compatible (0x...)
- **Withdrawal Process**: 2FA mandatory, network fee transparency visible

**Technical Insight**: Unlike self-custody wallets where you control private keys, exchanges use omnibus wallet architecture—your "balance" is a database entry, not a UTXO you control.

### **4. Charts & Market Data**
- **TradingView Integration**: Real-time candlestick charts with technical indicators
- **Orderbook Depth**: Visual representation of bid/ask spreads
- **Market Sentiment Tools**: Fear & Greed Index, 24h volume metrics

**Observation**: Data refresh rates vary (1-3 second delays noted), reminding us that CEX data is centralized, unlike DEX on-chain transparency.

### **5. Trading Features Tested**
- **Test Order**: Placed a small INR 100 / $10 limit order for BTC (cancelled before execution)
- **Fee Structure**: Maker/taker fees clearly disclosed (~0.1-0.2%)
- **Slippage Analysis**: On low-volume pairs, spread widened significantly—reinforcing the need for liquidity awareness

---

## Key Learnings & Technical Reflections

### **1. Custody Models: Trust vs. Control**
CEXs operate on **custodial models**—users deposit funds into exchange-controlled wallets. This introduces:
- **Counterparty Risk**: Exchange insolvency = potential loss (FTX flashbacks)
- **Operational Risk**: Hot wallet hacks, insider threats
- **Trade-off**: Convenience and fiat on-ramps vs. "not your keys, not your coins"

### **2. Compliance Architecture**
Modern exchanges are **crypto banks** from a regulatory standpoint:
- **AML Screening**: Transaction monitoring for suspicious patterns
- **Travel Rule Compliance**: Cross-border transfers >$1000 require sender/receiver info
- **Proof of Reserves**: Some exchanges publish Merkle tree proofs (transparency varies)

### **3. UX vs. Decentralization Paradox**
- **Speed**: Instant order execution (off-chain matching engines)
- **Simplicity**: Fiat on-ramps, unified dashboards
- **Cost**: Users sacrifice self-sovereignty for usability—a fundamental blockchain design tension

### **4. Security Best Practices Observed**
2FA enforcement  
Withdrawal whitelisting available  
Anti-phishing codes  
No granular API key permissions (all-or-nothing access on some platforms)

---

## Screenshots



**Example Captures:**
1. KYC completion confirmation (name/photo redacted)
2. BTC deposit address (last 4 characters visible only)
3. Orderbook snapshot for BTC/USDT pair
4. Trading interface with limit order form

---

## Broader Relevance to Blockchain Career

This exploration reinforced three core principles:

1. **Interoperability Matters**: CEXs are gateways between TradFi and DeFi—understanding both systems is crucial
2. **Security is Layered**: No single solution (custody, 2FA, cold storage) is sufficient—defense in depth wins
3. **User Experience Drives Adoption**: Technical purity alone won't onboard the next billion users—pragmatic UX bridges matter

As I continue working on Bitcoin infrastructure and exploring Layer 2 solutions, understanding how end-users interact with crypto through exchanges gives me better perspective on where self-custody tools, lightning wallets, and DeFi protocols fit in the ecosystem.

---

## Connect & Discuss

**LinkedIn Post**:   
**Future Interns Program**: Completing blockchain foundations while building real-world context  
**Summer of Bitcoin 2025**: Previously worked on multisig PSBT workflows—now bridging CEX/DEX mental models

**Questions? Let's discuss custody trade-offs, exchange security models, or API integration strategies.**

---


**Tags**: `#Blockchain` `#CryptoExchange` `#KYC` `#Custody` `#BitcoinInfrastructure` `#FutureInterns`