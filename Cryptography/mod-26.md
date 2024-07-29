# MY PROCESS

We are given an encrypted message:
- `cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_uJdSftmh}`

And a description:
- `Cryptography can be easy, do you know what ROT13 is?`

We just have to decrypt it using `ROT13` or `Caesar Cipher`

## SOLVING

I just inputted this on the terminal:
- `echo "cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_uJdSftmh}" | tr 'A-Za-z' 'N-ZA-Mn-za-m'`

And that will echo out the decrypted message which is the flag.
