# MY PROCESS

We are provided with an image file named `dolls.jpg`.

And since the title of the challenge is called `Matryoshka doll`, that got me thinking that there should be a hidden file within the image.

## SOLVING

What I did first is I ran `binwalk` on the image and this is the result:

![image](https://github.com/user-attachments/assets/a0fe6709-4c50-4cd1-8b03-f69c529cf4b1)

There is indeed a hidden file. I am going to extract it by doing `binwalk -e dolls.jpg` and this is the result:

![image](https://github.com/user-attachments/assets/e1f56bcb-f5ee-43ab-b308-c7b84c1a5fb3)

A file directory. And if you go to the file directory, there are two files:

![image](https://github.com/user-attachments/assets/67443087-dcd2-4a88-a7a4-05091a0cf13f)

A `zip` file and another directory. What I did is I went to the directory.

And inside of the `base_images` directory, we have another `.jpg` file.

![image](https://github.com/user-attachments/assets/9938bd1c-c42a-491b-97dd-43462faa3f37)

So, I used `binwalk` again to see if there are hidden files too since the challenge is `Matryoshka doll`.

![image](https://github.com/user-attachments/assets/f00237af-b676-4551-84d5-cc4b9ab88649)

There is another `.zip` file in the image. So I extracted it using `binwalk -e 2_c.jpg`.

And it will create another directory and then I apply the same thing:
- `cd <to the extracted directory>`
- `cd base_images`
- `binwalk <the image>`
- `binwalk -e <the image>`

Until I finally reached `4_c.jpg`.

After extracting `4_c.jpg`, instead of `base_images` directory, we have `flag.txt`.

![image](https://github.com/user-attachments/assets/f8e6cd92-ad57-44e3-aade-f9afc87574e1)

Read the text file and that will be the flag for the challenge.
