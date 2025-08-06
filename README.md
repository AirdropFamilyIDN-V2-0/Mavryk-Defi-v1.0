# 🧠 MAVRYK DeFi Bot v1.0

Automated DeFi strategy execution tool built on the **Mavryk Network**, enabling batch wallet processing for liquidity provision, vault creation, borrowing, repayment, and token staking (MVN) across multiple accounts.

## 🚀 Features

- ✅ Automated liquidity deposit
- ✅ Vault creation with MAV collateral
- ✅ Borrow and repay MAV from vault
- ✅ MVN staking with operator permission handling
- ✅ Multi-wallet execution via `privatekeys.txt`
- ✅ Live status logs with operation hashes
- ✅ Balance check with fallback handling
- ✅ Configurable delays and minimum gas check

## ⚙️ Configuration

The bot reads wallet private keys from a plaintext file:

```

privatekeys.txt

```

Example structure:
```

edsk...yourprivatekey1
edsk...yourprivatekey2
...

````

All key configuration parameters are defined directly in the script:

| Parameter                  | Description                           |
|---------------------------|---------------------------------------|
| `RPC_URL`                 | Mavryk RPC endpoint                   |
| `VAULT_FACTORY_ADDRESS`   | Vault factory contract                |
| `MVN_STAKING_CONTRACT`    | MVN staking contract address          |
| `LIQUIDITY_AMOUNT_MAV`    | Amount of MAV for liquidity           |
| `MVN_STAKING_AMOUNT`      | Amount of MVN to stake                |
| `MINIMUM_MVRK_FOR_GAS`    | Threshold MAV balance for operation   |

## 📦 Dependencies

Install via npm:

```bash
npm install
````

Dependencies:

* `@mavrykdynamics/taquito`
* `@mavrykdynamics/taquito-signer`
* `chalk`
* `fs`, `path`

## 🧪 Usage

Run the bot using Node.js:

```bash
node bot.js
```

The script will:

1. Read private keys from file.
2. Check balances for MAV, MVN, and tokens.
3. Perform liquidity + vault ops if balances meet thresholds.
4. Stake MVN via staking contract.
5. Print results + operation links.

## 📊 Sample Output

```bash
Loaded Private Keys : 5
Status              : Starting operations for 5 wallets...

Processing Wallet   : mv1abc123...

[1] Deposit Token
Token               : MAV
Amount              : 5 MAV
Tx Hash             : https://nexus.mavryk.org/operation/ooXyz...
Status              : Deposit successful

[2] Add Liquidity
...

🎉 All operations completed for all wallets!
```

## 📁 Structure

```
├── main.js               # Main script
├── privatekeys.txt      # Wallets input file
└── README.md            # This documentation
```
## 🔒 Restricted Access: VIP ADFMIDN Members Only

The **MAVRYK DeFi Bot v1.0** is an **exclusive tool for VIP ADFMIDN members** only.
To use this script, you **must have a valid license key** issued after successfully joining the VIP membership.

### 🎫 How to Get a License Key

To join the VIP program and receive your personal license key:

* 💬 Telegram: [@FxcTe](https://t.me/FxcTe)

> Each license key is **unique, non-transferable, and monitored** for misuse.

---

### ⚠️ WARNING

* Unauthorized use, distribution, or modification of this script is strictly prohibited.
* Violating the license terms may result in **permanent access revocation** and possible **legal consequences**.
* All license keys are actively verified and tracked via an automatic validation system.

---

### ✅ License Verification

This script will automatically **verify your license key** at runtime.
If the key is missing, invalid, expired, or unauthorized — all functionality will be disabled.

---




