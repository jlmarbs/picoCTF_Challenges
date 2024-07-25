# MY PROCESS

We are provided only with a binary file named ```out```.

From this my thought process is to try to find out if there are hidden things in that file.

## SOLVING

What I did first is that I used ```file out``` to know what kind of file that is.
![image](https://github.com/user-attachments/assets/e3fe9688-d1e5-4590-a9cc-f9e266403b8e)

From this one, I did not know on what to do with it so I used ```exiftool out``` to get more details.
![image](https://github.com/user-attachments/assets/8068ad19-2669-4698-ba10-89c1bfa10f3c)

Still no details, so I just randomly decided to do ```strings out``` to see if I am able to get anything from it.

![image](https://github.com/user-attachments/assets/78c05247-8de2-409d-b176-dfef5b52cb3f)

This caught me in the eye, it looked like an UPX executable packer, confirmed also in the contents of string:
![image](https://github.com/user-attachments/assets/427db05a-70c7-4d30-a60a-4896e120cfe4)

So what I did next is I used ```upx -d out``` to get something out from it.
![image](https://github.com/user-attachments/assets/3b21e346-4634-49c2-894e-29f8e2e31395)

Now I used ```file out``` again to see if anything changed.
![image](https://github.com/user-attachments/assets/f5d7001e-669f-43ea-8fea-d1f466733b24)

It did changed. Now it is time to look for the flag.

By doing so, I did ```strings out | grep "flag"``` if there are any flag contents in the file.
![image](https://github.com/user-attachments/assets/68eab21a-0857-445d-97e9-6622c91077a8)

The flag is there but it looks like a hex string, so we have to decode it.

What I did is that I did ```echo <hex 'string'> | xxd -r -p``` to decode the flag.

The output is the flag for the challenge.
