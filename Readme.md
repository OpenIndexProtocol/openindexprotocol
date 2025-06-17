# Open Index Protocol  
**Solana's modular index-fund engine** for creating and managing tokenized baskets of SPL assets.  
*Production-grade, open-source, and extensible via CPI modules.*

---

## 🌐 Overview  
Open Index Protocol enables **on-chain index funds** with:  
- **Tokenized baskets** - Mint/redeem diversified SPL asset portfolios  
- **Modular design** - Extend functionality via [`init_module`](https://openindex.gitbook.io/openindex#id-8-init_module) CPI interface  
- **Low-fee automation** - Optimized for Solana's speed and cost efficiency  

---

## ⚙️ Core Components  
| Component     | Description                                                                 |
|--------------|-----------------------------------------------------------------------------|
| `Protocol`   | Global state and module registry                                           |
| `Controller` | Administrative domain for multiple indexes                                 |
| `Index`      | Token basket (e.g., "Solana DeFi Top 5")                                   |
| `Vault`      | PDA-held SPL tokens backing the index                                      |
| `Module`     | Plug-in programs (e.g., Issuance, Trade, Rebalance)                        |


---

## 🧩 Modules  


### Coming Soon  
| Module            | Functionality                              |
|------------------|-------------------------------------------|
| `IssuanceModule` | Whitelists & fee hooks for compliance     |
| `TradeModule`    | DEX swaps via Jupiter/Raydium CPI         |
| `RebalanceModule`| Oracle-driven portfolio adjustments       |

*Build custom modules for yield strategies, NFT-gating, or DAO governance.*

---

### 📜 Architecture Doc
- [Architecture Gitbook](https://openindex.gitbook.io/openindex)
---

## 🚀 Getting Started  
### Prerequisites  
- [Rust](https://www.rust-lang.org/tools/install) + [Solana CLI](https://docs.anza.xyz/cli/install)  

### Build & Test  
```bash
git clone https://github.com/OpenIndexProtocol/openindexprotocol.git
cd openindexprotocol/open_index
cargo build-sbf
make test  # Unit tests
```

#### Integration Tests  
1. Start validator:  
   ```bash
   solana-test-validator
   ```  
2. Deploy:  
   ```bash
   solana program deploy target/deploy/openindex.so
   ```  
3. Test:  
   ```bash
   make test_validator
   ```  

---

## 📜 License  
Dual-licensed under **MIT/Apache 2.0** - No fees, no tokens, pure public good.  

