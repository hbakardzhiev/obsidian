## Machine readable address
- [[#public key hash]]
- [[#prefix]]
- *checksum*

### public key hash 
	-> hash(hash(*PubKey*))
**Note**: used hashing algorithm: 
- [*RIPEMD160*](https://www.nervos.org/knowledge-base/what_is-RIPEMD160_(explainCKBot))
- [SHA-256](https://www.simplilearn.com/tutorials/cyber-security-tutorial/sha-256-algorithm)
### prefix 
	-> the type of address that will be generated
- 00 -> [P2PKH](https://trezor.io/learn/a/pay-to-public-key-hash-p2pkh) locking script address
- 05 -> [P2SH](https://en.bitcoin.it/wiki/Pay_to_script_hash) locking script 
- 111 -> testnet *PubKey* hash
- bc1 -> Bech32 *PubKey* hash 
### checksum 
	-> substring(0, 4, hash(hash(*PubKey*)))
**Note**: SHA-256 is used as algorithm. 

## Human readable address:
- hash([[#machine address]])
	- **Note**: used algorithm [[Different bases#58 (Base58)]]