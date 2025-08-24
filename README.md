# DNS Wallet Tools

A web-based tool for checking wallet addresses and generating QR codes for DNS-based cryptocurrency addresses. Supports multiple DNS record formats for mapping cryptocurrencies to domain names.

## Supported Record Formats

These tools support 3 different DNS record formats for mapping cryptocurrency addresses to domain names:

1. **Type WALLET record** - Value: `COIN:address`
   - Reference: [IETF Draft](https://www.ietf.org/archive/id/draft-chins-dnsop-web3-wallet-mapping-01.html)

2. **Type WALLET record** - Value: `"COIN" "address"`
   - Reference: [IANA Template](https://www.iana.org/assignments/dns-parameters/WALLET/wallet-completed-template)

3. **Type TXT record** - Value: `coin:address`
   - Reference: [dprofile GitHub](https://github.com/H4ckB4s3/dprofile)

## Features

- **Wallet Checker**: Verify DNS records for cryptocurrency addresses
- **QR Code Generator**: Create QR codes for easy sharing of cryptocurrency addresses

## Adding TXT and WALLET Records on Shakestation

Shakestation (shakestation.io) is a DNS management interface for Handshake domains. Here's how to add TXT and WALLET records:

### Adding TXT Records

1. Log in to your [shakestation.io](https://shakestation.io) account
2. Select the domain you want to manage
3. Navigate to the "DNS Records" section
4. Click "Add Record" and select "TXT" as the record type
5. Enter the following format in the value field: `coin:your_wallet_address`
   - Example: `btc:1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa`
6. Save the record
7. Changes may take a few minutes to propagate

### Adding WALLET Records

1. Log in to your [shakestation.io](https://shakestation.io) account
2. Select the domain you want to manage
3. Navigate to the "DNS Records" section
4. Click "Add Record" and select "WALLET" as the record type (if available)
5. Enter the value in one of the supported formats:
   - Format 1: `COIN:your_wallet_address` (e.g., `btc:1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa`)
   - Format 2: `"COIN" "your_wallet_address"` (e.g., `"btc" "1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa"`)
6. Save the record
7. Changes may take some time to propagate through the Handshake network

### Supported Cryptocurrency Codes

Use these standard coin codes in your records:

- AAVE: `aave`
- ADA (Cardano): `ada`
- ALGO (Algorand): `algo`
- APT (Aptos): `apt`
- ATOM (Cosmos): `atom`
- AVAX (Avalanche): `avax`
- BCH (Bitcoin Cash): `bch`
- BGB (Bitget Token): `bgb`
- BNB (Binance Coin): `bnb`
- BTC (Bitcoin): `btc`
- CHAINLINK: `chainlink`
- CRO (Crypto.com Coin): `cro`
- DAI: `dai`
- DOGE (Dogecoin): `doge`
- DOT (Polkadot): `dot`
- ENA: `ena`
- ETC (Ethereum Classic): `etc`
- ETH (Ethereum): `eth`
- FIL (Filecoin): `fil`
- GT (GateToken): `gt`
- HBAR (Hedera): `hbar`
- HNS (Handshake): `hns`
- HYPE: `hype`
- ICP (Internet Computer): `icp`
- JUP (Jupiter): `jup`
- KAS (Kaspa): `kas`
- LEO (UNUS SED LEO): `leo`
- LN: `ln`
- LTC (Litecoin): `ltc`
- MNT (Mantle): `mnt`
- NEAR: `near`
- OKB (OKEx Token): `okb`
- OM (MANTRA): `om`
- ONDO: `ondo`
- OP (Optimism): `op`
- PEPE: `pepe`
- PI (Pi Network): `pi`
- POL (Polygon): `pol`
- RENDER: `render`
- SHIB (Shiba Inu): `shib`
- SOL (Solana): `sol`
- SUI: `sui`
- TAO (Bittensor): `tao`
- TIA (Celestia): `tia`
- TON (Toncoin): `ton`
- TRX (Tron): `trx`
- UNI (Uniswap): `uni`
- USDC (USD Coin): `usdc`
- USDE: `usde`
- USDT (Tether): `usdt`
- VET (VeChain): `vet`
- XLM (Stellar): `xlm`
- XMR (Monero): `xmr`
- XRP (Ripple): `xrp`
- ZEC (Zcash): `zec`

## Usage Examples

### Example TXT Record
Type: TXT
Name: @ (or subdomain)
Value: btc:1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa

text

### Example WALLET Record (Format 1)
Type: WALLET
Name: @ (or subdomain)
Value: ETH:0x742d35Cc6634C0532925a3b844Bc454e4438f44e

text

### Example WALLET Record (Format 2)
Type: WALLET
Name: @ (or subdomain)
Value: "HNS" "hs1qd42hrldu5yqee58s4d9grqsxqg5qgydytyyg4z"

text

## Verification

After adding your records, use the Wallet Checker tool to verify they're properly configured and accessible.

## Resources

- [IETF Draft](https://www.ietf.org/archive/id/draft-chins-dnsop-web3-wallet-mapping-01.html)
- [ANA Template](https://www.iana.org/assignments/dns-parameters/WALLET/wallet-completed-template)
- [Dprofile Profocol](https://github.com/H4ckB4s3/dprofile)
