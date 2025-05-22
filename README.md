# trust-crypto-wallet-tokenlist

Official token list for Trust Crypto Wallet UI - Multi-chain token metadata for secure digital asset management

## Overview

This repository contains the official token list for the Trust Crypto Wallet interface. The token list provides metadata for supported tokens across multiple blockchain networks, ensuring users can securely manage their digital assets with accurate information and trusted token verification.

## Files

- `tokenlist.json` - The complete token list JSON file
- `README.md` - This documentation file
- Token logo images in root directory (no logos/ folder needed)

## Usage

Import the token list directly from our GitHub repository:

```javascript
// Direct import
import tokenList from 'https://raw.githubusercontent.com/Trusx-crypto-wallet/trust-crypto-wallet-tokenlist/main/tokenlist.json';

// Or fetch in your application
const response = await fetch('https://raw.githubusercontent.com/Trusx-crypto-wallet/trust-crypto-wallet-tokenlist/main/tokenlist.json');
const tokenList = await response.json();
```

### Raw URL:
```
https://raw.githubusercontent.com/Trusx-crypto-wallet/trust-crypto-wallet-tokenlist/main/tokenlist.json
```

## Supported Networks

### Mainnet Networks
- **Ethereum** (Chain ID: 1) - Primary DeFi ecosystem
- **Bitcoin** (Chain ID: 0) - Native Bitcoin support
- **BSC** (Chain ID: 56) - Binance Smart Chain
- **Polygon** (Chain ID: 137) - Layer 2 scaling solution
- **Avalanche C-Chain** (Chain ID: 43114) - High-performance blockchain
- **Optimism** (Chain ID: 10) - Ethereum Layer 2
- **Arbitrum** (Chain ID: 42161) - Ethereum Layer 2

### Test Networks
- **Goerli** (Chain ID: 5) - Ethereum testnet
- **Sepolia** (Chain ID: 11155111) - Ethereum testnet
- **BSC Testnet** (Chain ID: 97) - Binance testnet
- **Mumbai** (Chain ID: 80001) - Polygon testnet
- **Arbitrum Goerli** (Chain ID: 421613) - Arbitrum testnet
- **Optimism Goerli** (Chain ID: 420) - Optimism testnet
- **Avalanche Fuji** (Chain ID: 43113) - Avalanche testnet

## Supported Tokens

### Major Token Categories

**Stablecoins**
- USDT (Tether USD) - Multi-chain
- USDC (USD Coin) - Multi-chain
- DAI (Dai Stablecoin) - Ethereum

**Wrapped Tokens**
- WETH (Wrapped Ether) - Multi-chain
- WBTC (Wrapped Bitcoin) - Ethereum
- WBNB (Wrapped BNB) - BSC
- WAVAX (Wrapped AVAX) - Avalanche

**Native Tokens**
- ETH (Ether) - Ethereum ecosystem
- BTC (Bitcoin) - Native Bitcoin
- BNB (Binance Coin) - BSC ecosystem
- MATIC (Polygon) - Polygon ecosystem
- AVAX (Avalanche) - Avalanche ecosystem
- OP (Optimism) - Optimism ecosystem
- ARB (Arbitrum) - Arbitrum ecosystem

## Trust Crypto Wallet Features

The Trust Crypto Wallet provides:

- **Secure Multi-chain Support** - Seamlessly manage assets across all major blockchain networks
- **Trusted Token Verification** - All tokens verified with official contract addresses and metadata
- **Safe Transaction Handling** - Proper decimal precision and amount calculations
- **User-friendly Interface** - Clear token identification with official logos and names
- **Reliable Asset Management** - Consistent token information across different networks
- **Real-time Updates** - Token list regularly updated with new tokens and network additions

## Token List Structure

Each token entry contains the following fields:

```json
{
  "chainId": 1,
  "address": "0xdAC17F958D2ee523a2206206994597C13D831ec7",
  "name": "Tether USD",
  "symbol": "USDT",
  "decimals": 6,
  "logoURI": "https://raw.githubusercontent.com/Trusx-crypto-wallet/trust-crypto-wallet-tokenlist/main/usdt-logo.png"
}
```

### Field Descriptions:
- **chainId**: Numerical identifier of the blockchain network
- **address**: Smart contract address of the token (or special address for native tokens)
- **name**: Full descriptive name of the token
- **symbol**: Trading symbol/ticker of the token
- **decimals**: Number of decimal places for token amount precision
- **logoURI**: URL to the official token logo image

## Token Count Summary

**Total Networks**: 13 (7 mainnets + 6 testnets)  
**Total Tokens**: 40+ tokens across all networks  
**Mainnet Tokens**: 16 unique tokens  
**Testnet Tokens**: 24+ test tokens  

## Version Information

- **Current Version**: 1.0.1
- **Last Updated**: May 21, 2025
- **Format**: Standard token list format
- **License**: MIT License

## Security & Trust

Trust Crypto Wallet prioritizes security and accuracy. All tokens in this list are verified for:

- ✅ **Correct Contract Addresses** - Verified against official sources
- ✅ **Proper Decimal Handling** - Accurate precision for calculations
- ✅ **Official Branding** - Authentic logos and naming conventions
- ✅ **Network Compatibility** - Tested across supported blockchain networks
- ✅ **Regular Updates** - Continuous monitoring and maintenance

## Contributing

We welcome contributions to improve our token list:

### Adding a New Token

1. **Fork this repository**
2. **Add your token** to `tokenlist.json` with all required fields:
   - Ensure correct `chainId` for the target network
   - Verify the contract `address` is accurate
   - Include proper `name`, `symbol`, and `decimals`
   - Provide a high-quality logo via `logoURI`
3. **Add token logo** to the repository root directory (PNG format, 200x200px recommended)
4. **Test the changes** to ensure JSON validity
5. **Submit a pull request** with a clear description

### Guidelines for Contributors

- Verify token legitimacy and avoid scam tokens
- Use official token information from verified sources
- Ensure logos are properly sized and high quality
- Test on appropriate networks before submission
- Follow existing naming conventions

## API Usage

### Fetch Complete Token List
```javascript
const tokenList = await fetch('https://raw.githubusercontent.com/Trusx-crypto-wallet/trust-crypto-wallet-tokenlist/main/tokenlist.json')
  .then(response => response.json());

console.log(`Total tokens: ${tokenList.tokens.length}`);
console.log(`Version: ${tokenList.version.major}.${tokenList.version.minor}.${tokenList.version.patch}`);
```

### Filter by Network
```javascript
// Get Ethereum mainnet tokens
const ethereumTokens = tokenList.tokens.filter(token => token.chainId === 1);

// Get all mainnet tokens
const mainnetTokens = tokenList.tokens.filter(token => 
  [1, 56, 137, 43114, 10, 42161, 0].includes(token.chainId)
);
```

### Search Tokens
```javascript
// Search by symbol
const usdtTokens = tokenList.tokens.filter(token => 
  token.symbol.toLowerCase() === 'usdt'
);

// Search by name
const bitcoinTokens = tokenList.tokens.filter(token => 
  token.name.toLowerCase().includes('bitcoin')
);
```

## Support & Contact

- **Issues**: Report bugs or request features via [GitHub Issues](https://github.com/Trusx-crypto-wallet/trust-crypto-wallet-tokenlist/issues)
- **Questions**: Open a discussion for general questions
- **Security**: Report security concerns privately via repository maintainers

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Disclaimer

This token list is provided for informational purposes. Always verify token contracts and do your own research before interacting with any cryptocurrency. Trust Crypto Wallet is not responsible for any losses incurred from using third-party tokens.

---

**Trust Crypto Wallet** - Your secure gateway to decentralized finance

*Empowering users with safe, reliable, and user-friendly multi-chain asset management*
