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
