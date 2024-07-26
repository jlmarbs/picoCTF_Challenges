# MY PROCESS

We are provided with a `pico.flag.png` file which looks like this:

![image](https://github.com/user-attachments/assets/9add422f-fc2c-468a-9063-3af5d274f348)

I tried running with `file` `binwalk` and `exiftool` to see if there is anything hidden in the details, but to no avail.

## SOLVING

I tried using `steghide` but it wouldn't make sense since we dont have a passphrase, and even submitting any passphrase will tell us that the file format is not supported for `steghide`.

![image](https://github.com/user-attachments/assets/0040e7d0-54da-4a7a-a0fd-7c2c9fc3c181)

Then I used `zsteg` to see if there hidden data in the image since it is a `.png` file.

![heccer](https://github.com/user-attachments/assets/85520bcc-3f5e-41a9-b7ab-03f3ef2c624b)

Indeed there is, and it confirmed that it is the flag since the hint said `We know the end sequence of the message will be $t3g0.`

That is the flag.
