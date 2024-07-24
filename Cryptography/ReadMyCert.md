# MY PROCESS

We are provided with a .csr file.

![image](https://github.com/user-attachments/assets/e84d84cd-3634-49e0-bca7-380a3d37d075)

Upon reading the .csr file, I have no clue whatsoever.

## SOLVING

What I did is that I copied the contents in the certificate request and input it on ```CyberChef```.
- I used From Base64 function for this one.

![image](https://github.com/user-attachments/assets/cd02daa7-4b7f-4c7d-8ec2-5f699ced99ec)

The flag for the challenge will be in the output.

## REALIZATION

I realized as well that we can actually use ```openssl``` to view the flag too.
- The command I used is ```openssl req -in readmycert.csr -noout -text```.
![image](https://github.com/user-attachments/assets/71ef5e8a-d6ba-449b-a385-7aaae450f16d)

The flag will be shown in the Subject CN.
