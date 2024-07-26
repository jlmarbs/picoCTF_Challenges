## MY PROCESS

We are given a zip file named `challenge.zip`.

This challenge uses `git` to find the flag of this challenge, so I think we have to extract it.

## SOLVING

After unzipping and going to the `drop-in` directory, we have this:

![image](https://github.com/user-attachments/assets/1c3bbe31-9179-4c32-8a8d-33336ea397a7)

A `message.py` file. But reading it will only result to this:

![image](https://github.com/user-attachments/assets/ea1ff600-7e48-42e9-89a2-eb8ce1735474)

Since we have to use `git` to find the flag, I did the command `git log message.py`.

You will find the flag in the `Author`.
