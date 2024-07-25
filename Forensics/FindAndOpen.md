# MY PROCESS

We are provided with a ```flag.zip``` and a ```dump.pcap``` files.

It says in the challenge that the zip file is protected with a password. And it says that the password might have been hidden in the ```.pcap``` file.

So I am going to start looking at the ```.pcap``` file.

## SOLVING

After opening the ```.pcap``` file in ```WireShark```, I am greeted by this on the first packet:
![image](https://github.com/user-attachments/assets/ebb15e2d-dffc-4eba-974c-e5a33b004d3c)

I don't know what that meant so I kept looking at the packets until I stumble upon this:
![image](https://github.com/user-attachments/assets/c666a6f0-85f4-4b4e-a57e-4216a881fb52)

And again, I do not know what that meant, so I kept looking again.

And then I encounted this:
![image](https://github.com/user-attachments/assets/3d2af406-59eb-4369-b7d7-3257f845c0a0)

At this point I have no clue whatsoever on what I should be looking for in this file, until I checked ```Packet No. 48```

I noticed that this packet has a unique protocol that can be nowhere found in the file since other unknown protocols were repeated many times.

![image](https://github.com/user-attachments/assets/65c9ff01-de00-46a7-a14e-23fdab4a53eb)

Checking the data and the hex below, I noticed that part of it looked like a base64 string.
![image](https://github.com/user-attachments/assets/6384e6fc-26a3-456c-bf42-aa4174fe8126)

So I copied the data as printable text and went to ```CyberChef``` and used the ```From Base64``` function. And this is what it looks like:
![image](https://github.com/user-attachments/assets/173651fe-3a1c-449c-9e16-bbd925b82f6f)

It showed the partial of the flag! But inputting this to the challenge will mark is as incorrect. So that got me thinking.
![image](https://github.com/user-attachments/assets/c666a6f0-85f4-4b4e-a57e-4216a881fb52)

This makes sense now since we got the partial of the flag.

So what I did is that, I inputted that as a password for the zip file.

![image](https://github.com/user-attachments/assets/fc8edcc8-ed24-4ef0-a39b-a93c8a1e5dee)

After inputting the partial flag as a password, it got extracted!

It will unzip a ```flag``` file which is a text file.

Upon reading the text file, that will be the complete flag for the challenge.
