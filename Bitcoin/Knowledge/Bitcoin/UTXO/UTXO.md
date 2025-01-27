User -> |zero|one|many| UTXO

### General properties
- If a UTXO is to be used, then it must be fully used
	- Example: UTXO holding 1 BTC and you want to send only 0.4 BTC to a friend. Then you must use the entire 1 BTC UTXO and then the change (0.6 BTC) you must send yourself back. Thus in fact you get a brand new UTXO having 0.6 BTC
- The balance that you see in a wallet for a given user is in fact a sum that is done by the software of the UTXO that the $PrivKey$ of the user can unlock
	- Example: User has UTXO holding 0.1 BTC, UTXO holding 0.2 BTC and UTXO holding 0.7 BTC. The user has $BTC_{WalletBalance} = 0.1 + 0.2 + 0.7 = 1.0$. 

### UTXO input

| Field                | Description                           |
| -------------------- | ------------------------------------- |
| **Transaction ID**   | hash of the transaction               |
| **Index**            | UTXO index in the transaction output  |
| **ScriptSig Size**   | size of the script unlocking the UTXO |
| **ScriptSig**        | UTXO unlock script                    |
| **~~Sequence num~~** | ~~deprecated~~                        |
