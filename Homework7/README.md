## Homework 7
#### Alexander Mathes
#### CNS

### Research a vulnerable service 
I chose to research UnrealIRCd 3.2.8.1. Unreal IRCd, is an open-source software package that provides the infrastructure for Internet Relay Chat (IRC) servers. IRC is a real-time chat protocol that allows users to participate in chat rooms and engage in private messaging.  This version of the Unreal IRCd program, however, featured a backdoor that was placed inside of the program.  It employs remote code injection where an attacker crafted a malicious payload disguised as an innocent IRC message and it is then sent to the server.  The server processes it and then it is executed, granting the attacker control which could range from initial unauthorized access, to having complete control of the server.  This all stemmed from a hidden backdoor that allowed malicious actors to take control.  The backdoor was introduced intentionally during the software’s development and allowed remote attackers to infiltrate IRC severs undetected.  The vulnerability posed a significant threat to the security and integrity of IRC servers.  The case serves as a study for understanding risks associated with hidden exploits and the significance of ongoing software maintenance and security best practices within the realm of relay chat servers.
https://www.unrealircd.org/docs/Main_Page
https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2010-2075

### Locate vulnerability information
There is 1 CVE on UnrealIRCd 3.2.8.1.  It is CVE-2010-2075.  This CVE is a Backdoor command execution which falls under the category of CWE-94 Improper Control of Generation of Code, also known as Code Injection.  The CVE is a form of code injection as the vulnerability allows an attacker to maliciously inject a payload disguised as a harmless IRC message.
https://www.exploit-db.com/exploits/16922
https://cwe.mitre.org/data/definitions/94.html
