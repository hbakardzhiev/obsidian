
| Field               | Dimension | Description                                |
| ------------------- | --------- | ------------------------------------------ |
| Block size          | 4 bytes   | Block size, expressed in bytes             |
| [[#Block header]]   | 80 bytes  | Block header, consisting of several fields |
| Transaction counter | 1-9 bytes | Number of transaction present in the block |
| Transactions        | Variable  | Transactions stored in the block           |


### Block header

| Field               | Dimension | Description                                                                                  |
| ------------------- | --------- | -------------------------------------------------------------------------------------------- |
| Version             | 4 bytes   | Version number. Used so that nodes can read correctly the content of each block              |
| Previous block hash | 32 bytes  | Used to prove the chain of blocks                                                            |
| Merkle Root         | 32 bytes  | Value of the root of transactions                                                            |
| Timestamp           | 4 bytes   | Unix time; the time of creation                                                              |
| Difficulty Target   | 4 bytes   | The difficulty of the Proof of Work algorithm for the block                                  |
| Nonce               | 4 bytes   | The counter used for the Proof of Work. This is what the miners try to find to get rewarded. |

