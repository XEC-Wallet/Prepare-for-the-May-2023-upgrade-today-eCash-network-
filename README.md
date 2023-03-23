# Prepare for the May 2023 upgrade today (eCash network)
Prepare your [XEC wallet](https://xecwallet.org) for an upgrade (On May 15th, 2023, the eCash network will upgrade).
![Logo](https://i.ibb.co/PWW2wLW/Logo-with-dark-blue-text.png)

When the median time of the last 11 blocks is over timestamp 1684152000 (12:00:00 UTC), the nodes running a version prior 0.27.0 will no longer be in sync with the [eCash](https://coinecash.org) network.
In order to keep running after May 15th, 2023, your node needs to be updated to version 0.27.0 or later.
Update early to keep your node in sync with the eCash network !

## Links

- [XEC wallet](https://xecwallet.org) - Official eCash wallet
- [XEC explorer](https://explorer.e.cash/) - eCash block explorer
- [XEC Price](https://coinmarketcap.com/currencies/ecash/) - eCash marketcap

### What features are included in the Network Upgrade?
#### Consensus-enforced transaction version
The version field of eCash transactions will be restricted to versions 1 or 2 by the consensus rules. This means that blocks containing a transaction with a different version number can no longer be mined. The purpose of this change is to pave the way for future implementation of a new transaction format. It will allow the new transaction format to use a version number that has never been used before in the eCash blockchain. This rule was previously enforced by policy, so no wallet update is required.

#### Miner fund moved out of consensus rules
The miner fund, part of the block reward that is funding eCash network development, will no longer be enforced by consensus. It will be enforced by policy, and a block that contains an invalid or no miner fund output will be rejected by Avalanche Post-Consensus. This will make it easier for updating the miner fund parameters such as the acceptable addresses.

#### Removed chained transactions limits
After the upgrade activates, Bitcoin ABC nodes will start accepting an unlimited number of chained transactions in the mempool. This was limited to 50 transactions before the upgrade. Note that this is a policy change and has no impact on the consensus rules.

### How do I upgrade?
The process of upgrading your node is straightforward: simply stop the currently running node, download the new version, and start the new version. Here are some example instructions for upgrading from version 0.26.13 to the latest version (0.27.1) on Linux:

- Shut down the node: ./bitcoin-abc-0.26.13/bin/bitcoin-cli stop
- Download the new version archive from the website: wget https://download.bitcoinabc.org/0.27.1/linux/bitcoin-abc-0.27.1-x86_64-linux-gnu.tar.gz
- Extract the archive: tar xzf bitcoin-abc-0.27.1-x86_64-linux-gnu.tar.gz
- Restart the node with the new version: ./bitcoin-abc-0.27.1/bin/bitcoind -daemon
- Clean up old version and archives (optional):
- rm -rf bitcoin-abc-0.26.13
- rm -f bitcoin-abc-0.26.13-x86_64-linux-gnu.tar.gz
- rm -f bitcoin-abc-0.27.1-x86_64-linux-gnu.tar.gz

More information: https://xecwallet.org
