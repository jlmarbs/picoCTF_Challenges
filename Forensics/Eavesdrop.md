# MY PROCESS

We are provided with `capture.flag.pcap` file.

In the hint, it said `All we know is that this packet capture includes a chat conversation and a file transfer.`

So that got me thinking that we should look at `TCP Stream` to find the flag.

## SOLVING

After following a `TCP Stream`, there will be a conversation exchanged:

![image](https://github.com/user-attachments/assets/90f05dff-7cf9-4fcd-82b3-405d0d35f30e)

So there are 2 clues that can lead to get the flag which are:
- `openssl des3 -d -salt -in file.des3 -out file.txt -k supersecretpassword123`
- `Oh great. Ok, over 9002?`

This got me thinking that we are going to use `OpenSSL` to decrypt the file.

But to find the file, the clue `Oh great. Ok, over 9002?` suggested that we should look at that stream with a port `9002` to get the `file.des3`.

After following the `TCP Stream` on port `9002`, we get this:

![image](https://github.com/user-attachments/assets/7297f8bd-b481-46cd-8be1-8cada7629f02)

What I did after that is I shaw the data as `Raw` and save it as `file.des3`.

![image](https://github.com/user-attachments/assets/c0f6ac88-e3f0-48fb-9ca3-88b945beaec6)

![image](https://github.com/user-attachments/assets/5a5a8666-dcdb-41f5-87d4-a2fb22b8154b)

Now, we can use the `OpenSSL` command to get the flag.

![image](https://github.com/user-attachments/assets/0e2455da-2796-4c04-8773-2d8f31bf064f)

Ther will be a warning but there is nothing to worry about.

The content of `file.txt` will be the flag for the challenge.


