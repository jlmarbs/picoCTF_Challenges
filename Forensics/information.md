# MY PROCESS

We are provided with a image file named `cat.jpg` and it looks like this:

![image](https://github.com/user-attachments/assets/eebb15d5-3c1b-4d46-8b21-9a54a5de9641)

And in one of the hints, We have to look at the details of the file itself.

## SOLVING

What I did first is I ran `exiftool` on `cat.jpg`.

![image](https://github.com/user-attachments/assets/f7bcec40-3d4a-4eb5-815c-a6155f7f65f7)

What I noticed here is that, the `License` looks like a `Base64 String`.

So What I did is I went to `CyberChef` and used `From Base64` function.

That will reveal the flag for the challenge.
