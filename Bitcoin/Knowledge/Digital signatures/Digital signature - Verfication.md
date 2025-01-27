To verify you need to generate $RandomPart$ and the $signature$ to proof one holds [[Bitcoin for devevelopers/Digital signatures/Digital signature - Creation#Private Key]]

1) Take the transaction and do the hash on it. Call it $h(msg)$ 
2) $p_1 = (x_1; y_1) = (h(msg) s-1 \mod n) * G$
![[Pasted image 20240801091903.png]]
3) $p_2 = (x_2; y_2) = (RandomPart / s-1 \mod n) * PubKey$   
![[Pasted image 20240801160313.png]]
4) Add $p_1$ and $p_2$: $Rv = (xv; yv) = p_1 + p_2$  
![[Pasted image 20240801160510.png]]
5) Given $c = xv \mod n$, check that $c == $[[Bitcoin for devevelopers/Digital signatures/Digital signature - Creation#Random part]]
	1) If the check is true, then the signature was made with the corresponding private key


