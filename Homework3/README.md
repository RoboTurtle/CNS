## HOMEWORK 3
#### Alexander Mathes
#### Computer Network Ssecurity
#### 14SEP23

### Distribution
For this homework I utilized Rhel 7.  It was completely through command line and used no GUI.
Rather than launching it from the Oracle VM Application, I used 'vagrant ssh' and did it entirely through there.

### Installation Process
First comes choosing a Linux host.  I chose the RHEL 7 image from the vagrant cloud website for no particular reason besides that it was something different.
Next we had to download the SCC.  I went on the cyber exchange website and in the library I chose  the corrosponding SCC.  I copied the link and used the
wget command in order to download it onto my VM.  I then download the packages for zip and unzip onto my distibution (sudo yum did not work) using wget on the packages and then using 'rpm -i <file>' in order to get them onto my VM.  I was then able to unzip the file.  The program was then downloaded into /opt/scc.

### SCC Scan Results
The SCC scan results produced a score of 34.38%  55 passed while 105 failed.  
There were a total of 5 CAT 1s that failed out of 21.

### Displayed below are screenshots of the SCC tool running on command line 
!![SCC tool use in command line](https://github.com/RoboTurtle/CNS/assets/70544712/e80f8b0d-725f-4cb1-a4df-57526ac62b21)

