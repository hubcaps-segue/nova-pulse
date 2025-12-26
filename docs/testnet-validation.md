# Nova Pulse — Testnet Validation Record

This document provides a sequential record of validation steps and results during deployments to **Base Sepolia**.

---

## Network Details

- **Network**: Base Sepolia  
- **Chain ID**: 84532  
- **RPC URL**: [https://sepolia.base.org](https://sepolia.base.org)  
- **Explorer**: [https://sepolia.basescan.org](https://sepolia.basescan.org)

---

## Validation Steps

### Step 1 — Network Configuration Verification

- [ ] Ensure that `chainId` is correctly set to **84532** for **Base Sepolia**.
- [ ] Confirm that the correct RPC URL (`https://sepolia.base.org`) is in use, and fallback is correctly configured.

### Step 2 — RPC Connectivity Test

- [ ] Fetch the **latest block number** to ensure the connection is live. The block number should be greater than zero.
- [ ] Retry the block fetch after a brief interval and confirm that the block number is incrementing.
- [ ] If RPC fails, switch to a fallback RPC (`https://base-sepolia-rpc.publicnode.com`) and confirm the issue is resolved.

### Step 3 — Read-only Probes

Using the **sample addresses** from `scripts/sample-addresses.json`, perform the following checks:

- [ ] Read **ETH balance** for `exampleEOA`. Should return a valid value (non-negative).
- [ ] Confirm **contract presence** for `exampleContract`. The returned code should be a valid contract bytecode or `0x` if no contract exists.
- [ ] Confirm that interactions with **zero address** return zero balances and **burn address** causes no errors.

### Step 4 — Explorer Verification

- [ ] Verify the **exampleEOA** address in the BaseScan Sepolia explorer and ensure it resolves correctly.
- [ ] Confirm the latest block number is synced with **BaseScan Sepolia**.
- [ ] Ensure **no Mainnet** references appear during testing on **Base Sepolia**.

---

## Conclusion

- [ ] All validation steps were successful on **Base Sepolia**.
- [ ] Ready for production deployment on **Base Mainnet** after final checks.

_Last updated: initial scaffold_
