*Way to prove that you own the private key but not hand it over*

## Digital signature has:
- [[#Random part]]
- [[#Private Key]]
- [[#The transaction data]]
-> $signature = (InclusionOfPrivKey + h(msg)) / (k - 1) \mod n$

### Random part
1) Calculate the order of point G of the second elliptic curve.
		-> According to [ChatGPT]: *the number of times you can add that point to itself before you return to the identity point (which is essentially the point at infinity)*
2) Generate a random number in the range - $[1; n - 1]$ and we call this number *k*
3) Multiply $k * G = (xr; yr)$. This is the random part, but only $xr$ coordinate is taken. 
4) $RandomPart=xr \mod n$ 

### Private Key
1) Calculate $InclusionOfPrivKey = RandomPart * PrivKey$ 

### The transaction data
1) Calculate $h(msg) = SHA{\text -256}(transaction)$  

