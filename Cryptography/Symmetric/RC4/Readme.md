# Introduction
RC4 (Rivest Cipher 4) is a symmetric stream cipher designed by Ron Rivest in 1987. It was widely used in SSL, WEP, and Windows applications, but due to multiple vulnerabilities discovered over time, it has since been deprecated and is no longer considered secure for modern applications.

# Working
<div align = "center"><img width="700" height="503" alt="image" src="https://github.com/user-attachments/assets/a828ae85-2bd3-4c90-9358-538766b3b11d" /> </div> <br>
<b>Encryption</b> :- The plain text and a secret key are provided by the user. The encryption algorithm uses the KSA (Key Scheduling) and PRGA (Pseuda Random Generation) algorithms to generate the keystream for the secret key that was entered. The produced keystream is XORed with the plaintext by XORing byte-by-byte as RC4 is a stream cipher and the encrypted text is recieved. 
<br><br>
<b>Decryption</b>:- The encrypted text obtained and the same secret key is inputted to decrypt the cipher text. The KSA and PRGA steps are repeated using the same secret key. The same keystream is regenerated and XORed with the cipher text byte-by-byte and the orginal text is recieved. 
<br><br>
<b>KSA</b>:- KSA initializes a 256-byte state array S[0..255] using the secret key. This array is later used to generate the keystream. 
<br>
<b>PRGA</b>:- PRGA uses the shuffled S array to generate a stream of pseudorandom bytes (the keystream) which will be XORed with the plaintext to produce ciphertext. 
<br>
<div align = "left"><p>( It would be more understandable in the code)</p></div>

