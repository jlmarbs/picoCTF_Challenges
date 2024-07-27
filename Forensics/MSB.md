# MY PROCESS

We are provided with a `.png` file that looks like this:

![image](https://github.com/user-attachments/assets/3f1dc271-a1a2-4aa5-adb0-a7de6db48af5)

In the description it says:
- `This image passes LSB statistical analysis, but we can't help but think there must be something to the visual artifacts present in this image...`

And in the hint it says:
- `What's causing the 'corruption' of the image?`

So I was thinking there might be hidden data MSB of the RGB pixel values of the image.

## SOLVING

I found a tool in GitHub that can extract data from MSB into a text file
- `https://raw.githubusercontent.com/Pulho/sigBits/master/sigBits.py`

But there were requirements for it to work which is
- `pip install Pillow`

After that, I inputted this command:
- `python3 sigBits.py --type=Msb --extract=CoLuMn <filename>`

And that will create an `outputSB.txt` file.

Upon opening it on a text editor, I did a `CTRL + F` to find the flag by using `"picoCTF"`.
- Alternatively, you can do this too `cat outputSB.txt | grep -o -E "picoCTF.{0.43} <sub>since doing the normal grep will not get you the flag.</sub>`

After doing so, you will get the flag for the challenge.
