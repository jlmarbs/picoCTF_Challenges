# MY PROCESS

We are given 2 files namely `capture.pcap` and `picopico.key`.

In the hints, it said that `How can you decrypt the TLS stream?`

That made me think that we should put the key in the wireshark to decrypt the TLS Stream.

## SOLVING

When I opened `Wireshark` and showed more details in the TLS, this shows up:

![image](https://github.com/user-attachments/assets/f1c3fbf5-d158-4381-a48c-11f0c5ff8e0a)

So, I tried following the `TCP Stream` first and this shows up:

![image](https://github.com/user-attachments/assets/67b72a2f-1758-4565-9d53-fec8e84f529f)

Everything was encrypted and so I tried to follow the `TLS Stream` and as I expected, it is empty

![image](https://github.com/user-attachments/assets/05d7d14a-4a87-4e60-8bc6-6b503b69435b)

Now we have to find a way to put the `picopico.key` on `Wireshark`.

After searching on the internet on how to, This is what I did:
- Go to Preferences `Ctrl + Shift + P`
- Go to `RSA Keys`
  - ![image](https://github.com/user-attachments/assets/2a807a21-bee6-484f-882f-1ae0c6298836)
- Add new key profile and choose `picopico.key`.

And now if you follow the TLS Stream, you can find your flag for the challenge there.

![tls](https://github.com/user-attachments/assets/ba3e0646-e961-43b7-abb5-882615b73a17)
<sub>pls dont view the commit history...<sub/>
