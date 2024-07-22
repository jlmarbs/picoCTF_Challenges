# MY PROCESS
*NOTE: THERE IS AN EFFICIENT WAY OF DOING THIS, MINE IS NOT*

Upon reading the given file, we are given a base64 encrypted text.
   ![image](https://github.com/user-attachments/assets/587ac0f5-77c5-469c-8ad6-f58359639cd3)
   
In order to get the flag, we must decode the message.

## SOLVING
- Run it in a base64 decoder ```base64 -d enc_flag```
  ![image](https://github.com/user-attachments/assets/76f1b94d-2d2d-457e-86ed-ce55841a15be)
  
  Now we are given still a base64 text but it's shorter.
- What I did was, I put the "decrypted" text onto another txt file. ```base64 -d enc_flag > output1.txt```
  - I did this 6 times...
    - The faster way of doing this is ```base64 -d enc_flag | base64 -d | base64 -d | base64 -d | base64 -d | base64 -d```
    - or a bash script that loops until it is solved.

After doing that, the flag will be provided.
