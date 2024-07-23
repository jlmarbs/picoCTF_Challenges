# MY PROCESS

We are provided with ```flag.png``` and it just shows us a picture of the picoCTF logo.

## SOLVING

So I tried ```exiftool``` the image, but there were no details that is useful to find the flag.
![image](https://github.com/user-attachments/assets/74921c04-f669-4e72-8573-00c0b53c9ce7)


So what I did is that, I tried using ```binwalk``` on the image, and this is the result
![image](https://github.com/user-attachments/assets/444b2342-69e4-4e36-86dc-f9984d5d70f9)

There is a hidden ZIP file in the image. To extract it, I did:
- ```binwalk -e flag.png```

That will show us that there will be a new file directory since we unzip the hidden ZIP file in the image.
![image](https://github.com/user-attachments/assets/3ed73377-4b58-443d-8be7-f0825d8c40ea)


I browse through the directory until I encountered ```flag.png``` on the ```secret``` folder.
![image](https://github.com/user-attachments/assets/b5b8f1a2-db82-4f7f-94fc-f80d77982dfb)

Opening the image will give you the flag for that challenge.
