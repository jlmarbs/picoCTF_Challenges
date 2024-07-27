# MY PROCESS

We are given a `.zip` file and after extracting it, we have this:

![image](https://github.com/user-attachments/assets/a82d7b27-6d7c-49aa-9ce2-7015d0d9fdf3)

And upon reading it, this is the result:

![image](https://github.com/user-attachments/assets/7f4075a4-1e79-4072-8d5b-31f04ee0079c)

We have to find the flag within that message through using `git`.

## SOLVING

So what I did is that, since I already know that we can `checkout` a commit ID, first thing I have to do is to get the commit ID.

I did `git log message.txt` to get the first commit ID.

![image](https://github.com/user-attachments/assets/439d377c-cd3f-4511-b165-12816244e42e)

Now I copied the commit ID and did this:

![image](https://github.com/user-attachments/assets/8f3bafd6-7946-4d65-83ab-29654581c470)

It will give us a note on how to revert back to the latest commit if you're done.

Read the `message.txt` and you'll get the flag.
