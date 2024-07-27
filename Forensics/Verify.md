# MY PROCESS

We are given a zip file or if you launch the instance, it will provide you with a SSH connection with the same files in the zip file.

And when also running the instance, we are given a clue on what file with the same checksum to check.
- ```Checksum: 5848768e56185707f76c1d74f34f4e03fb0573ecc1ca7b11238007226654bcda```
- This can be also viewed on the file itself ```checksum.txt```.

## SOLVING

What I did is that, after unzipping the files, I went to the 2nd to the last directory which was ```../drop-in```.
![image](https://github.com/user-attachments/assets/58aa0636-e625-4572-9351-e0b1c1c9812d)

This is the content inside of the drop-in directory.

Since we are provided with the checksum to check what file we need to decrypt, I take a look first on the .sh file.
![image](https://github.com/user-attachments/assets/b7c0d1ec-1951-4507-9936-7c69defdbf59)

It is basically a shell code to decrypt the right file. To make it executable, I just did ```chmod +x decrypt.sh```.

Before we are going to use the shell file, we must first check what file has the same checksum with the provided checksum.
- The command I used is ```sha256sum files/*``` <- that is to view everything inside files directory.

![image](https://github.com/user-attachments/assets/47b84086-9ccf-462b-b5ed-df557cb395a2)

<sub>The lists of files goes on and on</sub>

Since there are a lot of files there and we just need to check for the same checksum provided, This is the command I used:
- ```sha256sum files/* | grep "<the checksum provided to us>" ```
![image](https://github.com/user-attachments/assets/f8696aad-edef-4580-a6fb-63aec5ab5fb3)

This will be the result.

Now since we know that we need to decrypt ```8eee7195```, we can now go back to the shell file that we made executable.

I run it with ```./decrypt.sh files/8eee7195``` <- will only work if you connect with the provided SSH!

After that the flag for that challenge will be revealed.
