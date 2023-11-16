## HOMEWORK 8
#### Alexander Mathes
#### CNS
#### 15NOV2023

### Security tool research

The tool I decided to base most of my exploit on was Burpsuite.  Bursuite can be downloaded at https://portswigger.net/burp/documentation/desktop/getting-started/download-and-install and the installation instructions are on there as well on the portswigger site.  Burpsuite is written in Java.  Burpsuite is a web application security tool and boasts a comprehensive set of features for finding and exploiting security vulnerabilities in web applications.  Some key functions and functionalities that burpsuite offers are proxies which interceps a user's browser and web application, intruder, which is used for performing automated attacks such as brute forcing or fuzzing, repeater, which allows a user to repeat and modify individual requests to test and analyze input scenarios, comparer, a tool used to highlight differences between two HTTP requests or responses, a built in browser that automatically connects with the bursuite application, scanner, an automated scanner that crawls through a web application and identify common security issues such as SQL injection, cross site scripting, and more.  Overall, burpsuite is a powerful tool that can help identify vulnerabilities on a web application and help take advanatge of those vulnerabilities.  I planned to utilize burpsuite and its function to proxy a login page and intercept a request and to then use intruder to bruteforce a worlift for the username and password administrator credentials.

 ![Screenshot 2023-11-15 230106](https://github.com/RoboTurtle/CNS/assets/70544712/ed26ac3c-55ba-49ff-a832-2ebc701b68d7)
 Screenshot displays GUI for burpsuite running on my Kali host.

### Use of chosen tool

For my exploit, I decided to do the difficult module and attack a seperate host located on the same network.  For this attack, I would be attacking a login page on a website.  The first thing I did was scan port 80 using the masscan tool to check if anything was running.

![Screenshot 2023-11-15 225934](https://github.com/RoboTurtle/CNS/assets/70544712/080fd06f-2f11-49bc-95f3-5f467356f77e)
As dipicted in the screenshot, I realized that a web service was in fact running on port 80.

I loaded up burpsuite and accessed the built in browser.

![Screenshot 2023-11-15 230238](https://github.com/RoboTurtle/CNS/assets/70544712/f7501e0a-3bb0-4b25-8b68-f58fa9be95c7)

From here, I went to the URL and typed in the IP that the service was being hosted on as well as the respective port.

![Screenshot 2023-11-15 230416](https://github.com/RoboTurtle/CNS/assets/70544712/3f5f06c5-82e8-4f2d-9098-3a01f0d304a3)

I navigated to the DVWA (Damn vulnerable web app) link as it was the service I intended to exploit.

![Screenshot 2023-11-16 003338](https://github.com/RoboTurtle/CNS/assets/70544712/d5db2e30-a345-46da-96ce-3a00e74e871e)

Once I clicked on the page I was presented wioth a login page, to which I began my proxy intercept in my burpsuite GUI.

![Screenshot 2023-11-16 003403](https://github.com/RoboTurtle/CNS/assets/70544712/11bbfd12-c5f5-447b-9aff-940966c2920a)

Due to some intercept issues with the site and its requests I had to make some adjustments in relation to what the proxy actually intercepted.  Particulary, the request interception rules where I made it intercept only a specific heading.

![Screenshot 2023-11-16 004408](https://github.com/RoboTurtle/CNS/assets/70544712/1e1194dd-8577-492b-aab8-4f28524faae4)

After ensuring I set up my proxy properly, I intercepted a login request and sent it over to the intruter, where I marked the input for username and password as payload positions and setting the attack type as cluster bomb, which would allow me to go through each username with each password.

![Screenshot 2023-11-16 003457](https://github.com/RoboTurtle/CNS/assets/70544712/99faba9a-ab91-4997-9f49-c3f71db6c8ec)

I then switch over into the payloads tab and setup payload position to a applicable worlist.  After doing so I hit the attack button and began the bruteforce.

![Screenshot 2023-11-16 003653](https://github.com/RoboTurtle/CNS/assets/70544712/f9bc8059-ce08-425e-96bc-b137a0a47353)

Going through some of the results, I noticed that one particular attempt was different than the rest in the fact that in the results section, most had the result Location end up being login.php again, representing that after the associated attempt, the page would go back to the login page, but for the instance where the username was "admin" and the password was "password" it would instead take me to the login.php location instead.  This is further back by the output of the actual login page after the requests were forwarded. 

![Screenshot 2023-11-16 003744](https://github.com/RoboTurtle/CNS/assets/70544712/770ed230-30ce-4be3-bf0f-f4f546b65e01)

I put in the username and password that gave me the unique results.

![Screenshot 2023-11-16 003802](https://github.com/RoboTurtle/CNS/assets/70544712/4a3ba8dd-a4d7-4e7f-b9dc-170f473b1323)

This resulted in letting me login as the Administrator user, displaying a successful exploit using Burpsuite.

![Screenshot 2023-11-16 003828](https://github.com/RoboTurtle/CNS/assets/70544712/13f80361-29a8-4f6a-abbe-9dffa177efef)





