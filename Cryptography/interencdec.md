# MY PROCESS

We are provided with a file named ```enc_flag```.

And viewing in the hints made me think that we are going to decode ```enc_flag```.

## SOLVING

What I did first is I read the contents inside ```enc_flag``` first.
![image](https://github.com/user-attachments/assets/800d1644-bdc6-4635-a633-a4f364c18c6e)

This shows a base64 string that we need to decode.

The command i used is ```base64 -d enc_flag > output.txt```
![image](https://github.com/user-attachments/assets/4e021b52-ff81-4fbb-9ab9-90e0fe105f40)

This is the result. Note that it is still also a base64 string, so I decoded it again.

But before I decode it again, I noticed that when I do the base64 decode command, it will return gibberish to me.

So in order to avoid that, I removed ```b' '``` in the output.

Then I run the command again ```base64 -d output > wah.txt```
![image](https://github.com/user-attachments/assets/5a7a150e-f5dd-40cb-96e8-b869628e88de)

Reading the file will result into that.

By viewing at the file, it looks like a Caesar Cipher. 

So what I did is that, I tried all possibilites ```e.g ROT13 ROT14 ROT15 and so on```.

It looked like a ROT19 encryption so this is the command I ran to decode it:
```cat wah.txt | tr 'A-Za-z' 'T-ZA-St-za-s'```

Upon doing that, the flag for that challenge will be revealed.
