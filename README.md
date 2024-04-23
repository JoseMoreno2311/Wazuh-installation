Hello everyone! If you managed to get up to this point, I believe it's because you're leap of interest at what Wazuh is capable of. Go through the step by step and feel the fabulous experience of gathering, processing, and linking real time security events. 

The architecture of Wazuh is distinguished by its flexibility and, extendibility that makes it real performer for small businesses and big organizations. Wazuh is not only an effective security solution but also is an open-source project with a unified agent and platform architecture which eliminates the previous separation of the functions. Such integration is a total fence guarding both public and private cloud infrastructures, including the local data center. 


And here's the exciting part: Hang around as I demonstrate the installation of Wazuh and its Windows agent in quick succession. Alongside, let’s help you sail through this and encourage you to enjoy leveraging the strengths of Wazuh by exercising the appropriate cybersecurity measures. Are you all prepared to begin this adventure to the world of cybersecurity with me? Stay tuned!
Let's open the link that contains the documentation for installing our agent.


https://documentation.wazuh.com/current/deployment-options/virtual-machine/virtual-machine.html#virtual-machine-ova


 ![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/526b5b32-46fb-4049-9d7f-fde35295ea65)

 

The virtual appliance (OVA) is the link that contains the necessary components for our installation. It includes Amazon Linux 2, Wazuh Manager 4.7.2, Wazuh Indexer 4.7.2, Filebeat-OSS 7.10.2, and Wazuh Dashboard 4.7.2. All of these come compressed in the same document, so we won't have to go through the installation process one by one. Wazuh requires the host machine to be a 64-bit system with 4 CPU cores, 8GB RAM, and 50GB storage. 


![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/6fba5f4d-f6b4-428e-be86-4cb83fd6535f)



Once we download our archive, we'll open our VirtualBox, and simply opening the Wazuh-4.7.2.ova will be enough to kickstart our installation. 

![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/8aea18ae-aa56-42c0-885d-250e13c3f3dc)


After opening our Wazuh 4.7.2 OVA file in VirtualBox, the software guides us through the installation process. It sets default values for CPU (4 cores), RAM (8GB), and Storage (50GB) as mentioned earlier. We press 'Finish' and wait for our Wazuh installation to complete. 

![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/09e714ff-9c7b-4cf8-b6e3-d570667d6213)



The documentation advises us to change the graphics controller; by default, it is set to VBoxVGA, and we will switch it to VMSVGA to ensure optimal performance for our agent. 

![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/30aba6fd-482e-44d3-aa25-10da3e027284)


Remember to configure our network as a bridged adapter so that we can maintain a direct connection to our host computer. Let's start our Wazuh 4.7.2 OVA machine. 

![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/b6d5b5b9-ad24-4068-a752-bd981668237d)


After booting the machine, we can get the login which does not come by default on the machine, also in the documentation. This is User: wazuh-user Password: wazuh.

![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/f78528bd-c86f-42ed-a51e-1f77f61fb9e3)


 
After entering the credentials mentioned above, we would only need to type the command "ip a" which refers to "ip address" and thus be able to know what ip address wazuh has assigned for our virtual machine, in this case it is 192.168.1.6. 

![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/47ed9a57-5528-44e7-bd3b-2aef3cdb18cb)



After getting the ip, you can just redirect to your preferred browser, either Chrome, Edge, Brave, Firefox, etc. In this case I am using brave. Accept the certification terms in Advanced and then proceed.

![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/f4057103-85b2-410d-89f1-e5d1ee2e660e)


 
Here we have accessed Wazuh successfully, now we put the credentials that wazuh offers us in the documentation, this would be. User: admin Password: admin 

![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/c03d4193-0738-4fed-a1ec-2361fb728030)





We have accessed our wazuh portal, the next steps will be to activate our agent.. 

This agent will be set up using our Windows 10 Virtual Machine. In this step, we will only download the ISO image of the machine we are going to use. I will provide the URL for easier access.
https://www.microsoft.com/en-us/software-download/windows10


![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/2334564c-8304-4ce2-b1cb-174bcd14a081)


Select 'Download Now,' and the Microsoft tool will automatically start downloading. 

![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/a67fb9a8-4655-4723-9c80-dd3d5a11718a)


"Choose ‘Create Installation media (USB flash drive, DVD, or ISO file) for another PC.' Then, select 'Next.'
 
![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/0e49077c-2ad8-4747-b833-03ec9f9611cf)

This is the Windows version to download; personally, I prefer not to choose the recommended options for this PC since it will be used as a Virtual Machine. Select 'Next' and wait until our ISO image is downloaded.

![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/850eb85d-c984-4532-9e7f-c931d694e5d4)

 


Once we have our ISO image, head to VirtualBox. Simply input the name (keeping the default folder), and for now, do not select the ISO image; we will install it manually. Choose 'Microsoft Windows' for the type, and the version to install is 'Windows 10 (64-bit) 

![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/d2d7029d-2774-44bb-bd01-4df1b452b448)

Personally, I prefer allocating sufficient memory to Windows since it will serve as our agent for Wazuh. We want it to run smoothly.. 

![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/259ec995-b525-441f-8e69-493cee4017c1)

 
Processors (5) 

 ![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/a61d49f4-aebd-4e3f-8dc6-b89ec7f67852)


One of the crucial points in our configuration is the Storage setting. Here is where we attach our ISO image to the 'Empty' disk. Simply select 'Empty,' go to the disk icon, and browse for the Windows 10 ISO image we downloaded from the Microsoft website. Confirm the selection, and start our Windows 10..

 ![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/df9873d3-ecbc-47e5-87fd-a982897fdd9e)


Here, choose the language of your preference; in this case, English (United States)."
 
![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/83f53fd1-ba4c-4cab-afaf-c3570ac58ea1)

Select 'I don't have a product key' and proceed.

![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/9f4b08ae-e9f1-4482-9f43-dfed472f0af5)


Choose Windows 10 Pro
 
![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/04f818e7-5bca-452e-beef-3e81dbccb6a0)

Select 'Custom: Install Windows only (advanced).

![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/1f5fb897-3a92-4790-a5c1-47f4128c0444)


Choose the disk we created, in this case, I created it with 50.0GB, but it could be a minimum of 20.0GB.


![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/99b9bb97-67a8-4c3c-a2c0-596904cb9065)


 

Now that we have our Windows 10 ready, let's go to the main Wazuh screen. Log in with the user: admin, password: admin. Choose 'Windows' and use the IP address provided by Wazuh, in my case, it's 192.168.1.6. For an optional setting, you can name it 'Windows10,' but you can choose any name you prefer. In my case, I'll name it 'windmachine’ .

 ![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/472ce690-ef37-4b08-90de-578e00e37b77)


Our main mission is to have this command ready to be used in the PowerShell of our Windows 10 VM

![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/1b6c4c8d-5e7a-4854-bb17-b3625b66a8b7)


Now that we've entered our code in PowerShell, we simply start the machine.
 
![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/b7465140-389d-4289-ad21-56b723321149)

After starting our service, we return to Wazuh and ensure that the agent is fully added.

![image](https://github.com/JoseMoreno2311/Wazuh-installation/assets/167577270/cbbd97ca-f6b4-43ed-aad9-28ce90f63b29)

And thus, we conclude our installation of Wazuh and its Windows 10 agent on VirtualBox. I hope you enjoyed this setup. Stay tuned for more projects using this fantastic platform. Thank you very much for your attention! If you have any questions, feel free to reach out to me via LinkedIn: https://www.linkedin.com/in/josemoreno2311/











