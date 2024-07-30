# MY PROCESS

We are given a `.pcapng` file which we can open by using `Wireshark`.

There is no hint on the given challenge so I assumed that the flag is within the streams but I do not know what protocol.

## SOLVING

I opened the `.pcapng` file using `Wireshark` and followed a `TCP Stream`.

![image](https://github.com/user-attachments/assets/1ad4b137-617a-48aa-a058-2a732a9355f7)

There is nothing unusual here since everything was encrypted. So I increased the number of Stream.

![image](https://github.com/user-attachments/assets/05d0490b-3177-4908-8d96-ac0c4a2bd4ee)

Nothing too here. So I increased the stream up until I reached Stream 5.

![image](https://github.com/user-attachments/assets/8c6bbca3-0dc7-4a3c-b5fa-a0b908fc5b68)

There is a text that has a similar format of the flag which was `cvpbPGS{c33xno00_1_f33_h_qrnqorrs}`.

It looked like a `Caesar Cipher` so I decoded it in the terminal using `echo "cvpbPGS{c33xno00_1_f33_h_qrnqorrs}" | tr 'A-Za-z' 'N-ZA-Mn-za-m'`.

That will decrypt it and show you the flag for the challenge.
