# MY PROCESS

After unzipping the file, we are provided with an IMG file. Our task is to get the flag within the picture.

## SOLVING
I used ```exiftool``` on the picture to see if I can get more information about the file.
![image](https://github.com/user-attachments/assets/2eaf1a2d-4f9f-4650-bcf4-29d4ac8141a4)

As you can see, the Attribution URL looks like a base64 string.
Once I copied the Atrribution URL, 
I went to ```CyberChef``` and used ```From Base64``` function.

After doing so, you will get the flag for that challenge.
