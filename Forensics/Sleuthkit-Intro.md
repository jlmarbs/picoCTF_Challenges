# MY PROCESS

We are given a `gzip` file and tasked to find the size of the `Linux Partition`.

And then after launching the instance, we are given a server to check the answer in order to get the flag.

## SOLVING

I extracted the `gzip` file first by doing `gzip -d <filename>`.

![image](https://github.com/user-attachments/assets/6cd7d800-c246-496e-b557-4c55c382672f)

This is what we get afterwards. And then I used `mmls` to check for the size:

![image](https://github.com/user-attachments/assets/4a444fa8-d0d0-4a64-a3ed-786630f11f51)

The length on `002` is the size of the `Linux Partition`.

After that I connect to the server provided and enter the size

![yeee](https://github.com/user-attachments/assets/cbbddb6d-6454-4fb1-8766-9ff9d484fba4)

Below the `Great work!` is the flag for the challenge.
