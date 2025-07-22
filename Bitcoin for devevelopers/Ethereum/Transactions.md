If a sender of a transactions has more *Gas* than necessary then the *Gas* that is left is returned to the sender.
Example:
![[Pasted image 20240808181628.png]]
If the sender of the transaction does not have enough *Gas* then the state of the transaction is fully reverted.
![[Pasted image 20240808181726.png]]In this case no *Gas* is returned to the sender.
