# MY PROCESS

We are provided with a picture called ```atbash.jpg```.

![image](https://github.com/user-attachments/assets/7a24a15f-9633-4ba7-843f-98e5674de270)

This tells me that we are going to use Atbash Cipher to decode something.
But since there is no text to be decoded, we have to find it within the image.

## SOLVING

What I did is I did ```steghide extract -sf atbash.jpg```

![image](https://github.com/user-attachments/assets/9bda1d74-a407-4f5e-b7a2-e84a6c8e16e7)

Then it will ask for a passphrase.

This is where I was stuck for a long time and then decided to press enter without typing anything.

As a result, we actually got a text file called ```encrypted.txt```

![image](https://github.com/user-attachments/assets/999d835d-0e1f-4de6-ba5d-5f9cd0bc10fb)

We are now provided with something to decode using Atbash Cipher.

I went to this website ```rumkin.com/tools/cipher/atbash/``` to decode.

Upon decoding, the flag will be revealed.
