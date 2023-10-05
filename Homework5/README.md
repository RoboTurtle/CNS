## Homework 7
#### Alexander Mathes
#### CNS
#### 05OCT2023

### Section 2

![Screenshot 2023-10-04 233630](https://github.com/RoboTurtle/CNS/assets/70544712/ab4ffe93-1ec2-4f60-99a0-16f0d0a08801)

Above it displays me running the command w --from while acting as user 'root' which displayed information such as what user I was, what ip I was from, My login time, and more.

![Screenshot 2023-10-04 233444](https://github.com/RoboTurtle/CNS/assets/70544712/f22c37b6-ccbc-4e30-baf4-31925ae4da2c)

Above shows me using ssh in order to directly get the hostname without actually going in.

![Screenshot 2023-10-04 235059](https://github.com/RoboTurtle/CNS/assets/70544712/942498db-6916-49dc-9b0b-2519809d5b57)

Above shows me using the ssh-copy-id command in order to copy over the rsa key i just generated into a file.

![Screenshot 2023-10-04 235520](https://github.com/RoboTurtle/CNS/assets/70544712/e901a444-7761-4933-883c-b57ce01f0427)

Above shows me using an ssh with an rsa key but stored is a different file than usual and it actially needing a password that I had set.  
I am also just using it to get the hostname and not to actually go into servera.

### Section 3

![image](https://github.com/RoboTurtle/CNS/assets/70544712/2a89b772-a29e-43ed-91c3-70e732c066ad)

Above shows me using ssh-keygen in order to generate an rsa key

![image (1)](https://github.com/RoboTurtle/CNS/assets/70544712/216d4960-585f-45e5-9460-84d6e511504e)

Above shows me using the ssh-copy-id command in order to apply the rsa key on the jumpbox

### Section 4

![image (2)](https://github.com/RoboTurtle/CNS/assets/70544712/a0cd7ba6-9fc6-41e9-b115-3b3a4bd3a140)

Above shows me going into the jump box and changing my password.  I changed it to Monkey.

![image (3)](https://github.com/RoboTurtle/CNS/assets/70544712/41298cab-6722-4dda-afc3-20f70355c697)

Above shows me running the hydra program in order to brute force my password on the jumpbox. 
I used a wordlist provided on the Seclists github.









