# MY PROCESS

After launching the instance, we are provided with 2 servers and tasked to get the flag by basically abusing the machine.

## SOLVING

If I connected to the 2nd server (in my case it was `tethys.picoctf.net 49943`), it asked for a password:

![image](https://github.com/user-attachments/assets/5921d080-e7c2-4730-aa0d-483e55d8dc64)

But we do not know yet the password. So that got me thinking what if we are going to connect to the first server?
- In my case it was `tethys.picoctf.net 58248`.

![image](https://github.com/user-attachments/assets/b8a5bc63-a05c-4144-bbe4-37d783a39064)

And there is our password, `My_Passw@rd_@1234`.

After inputting the password, we are asked with another 2 questions and here are the answers:

![image](https://github.com/user-attachments/assets/aff3ce24-9a8f-42d8-bc75-1e151b011fc2)

First thing I did is I went to the root directory:

![image](https://github.com/user-attachments/assets/38e82c64-e17e-4e5a-876c-9cb7a0bbbf4c)

I saw 2 files namely `flag.txt` and `script.py`.

I tried reading the flag but I got denied:

![image](https://github.com/user-attachments/assets/f53e421d-b6bb-4e8c-8850-b0ebae9e27f5)

So I went to read the python script and noticed this:

![image](https://github.com/user-attachments/assets/3df1c01d-93a9-496c-960b-f9ca27a2a685)

This was the hint suggested that we need to use `symlinks` since `symlinks` acts as a reference pointers to files or directories.

So what I did is that, I went to the player directory and did this commands:

![image](https://github.com/user-attachments/assets/16de3c6b-ee56-4540-92fe-4d58d6fa2ff9)

- The symlink command here was the `ln -s <filepath> <linkname>

Then if you try connect to the server again, the banner will the be flag of the challenge.
