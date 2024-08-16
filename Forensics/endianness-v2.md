# MY PROCESS

We are provided with the file named ```challengefile```.

## SOLVING

What I did first is I ```exiftool``` the ```challengefile``` and it looks like this
![image](https://github.com/user-attachments/assets/3c4ba96e-552a-4acf-b97b-fb48f6decd34)

Upon looking at the details, I noticed that there is a warning saying that it contains a JPEG byte header.

So what I did is I opened the file using ```ghex```
![image](https://github.com/user-attachments/assets/8f43ef4a-b36c-479d-a56d-63ab1f475e98)

I noticed that the first 4 bytes is a reversed of a JPEG header.

So what I did is that, I entered this command to get the flag: 
- ```hexdump -v -e '1/4 "%08x"' -e '"\n"' challengefile | xxd -r -p > output_file```

Now I did ```exiftool``` on the output to see the details.

![image](https://github.com/user-attachments/assets/f5e2a90e-c0eb-46a5-8f0f-c87d8f75326c)

Since it is a JPEG file, i renamed the file by doing ```cp output_file flag.jpg```

After opening the ```flag.jpg``` you will get the flag for that challenge.
