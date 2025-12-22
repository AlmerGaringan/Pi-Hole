# Pi-Hole
A Pi-hole is a network-wide ad blocker and a DNS filter. The reason I decided to build a Pi-Hole is to block the ads that are in my network. I learned a lot through this project; some of the key concepts I acquired include DNS, Linux, and IP addressing. 
<img width="1066" height="600" alt="Screenshot (102)" src="https://github.com/user-attachments/assets/3fd9718b-fb90-4151-bc03-e505554d7202" />

## Hardware & OS

- Travel router

- Wireless Ethernet adapter. 

- Raspberry Pi OS and Ubuntu Server

## Installation 

The first command when I was building this project was;

```
sudo apt update
```
then
```
sudo apt full-upgrade
```

The first thing I did was update and fully upgrade my system. This allows your Pi packages to be fully updated to make sure they're up to date. 

Then I ran this command;

```curl -sSL https://install.pi.hole.net | bash ```


Curl is used to fetch or retrieve the data in that URL or from the server, and then -sSL: -s means silent mode, -S only shows errors, and -L means any redirection 

Bash receives what the curl command wants to fetch, then turns that input into text and runs the script line by line. 

After you type this command in, an installation wizard will pop up. This will allow you to customize your Pi-hole. 

In your router interface, you want to go to your DNS server settings and manually type out your Pi-hole IP address. A way to find out your IP address is by completing your installation then which gives you your IP address, and it will be shown something like this: IPV4: (IP Address). 

![5836FCA6-D6AA-42A0-BBA6-905BCFFA568F](https://github.com/user-attachments/assets/79398870-9ecb-4e79-8242-1022c46025d0)

another way of finding out your Pi-hole IP address is through the CLI and putting;

```ip addr```


This will give you all of the IP addresses on your Pi. So whatever interface you choose during the installation, whether it’s wlan0 or eht0 or some other one. The IP address will be under whatever you choose. 

After this, I enabled my DHCP settings in my Pi Hole admin. In this, you will get a range of IP addresses to hand out from start to end, then you also have to put your Router IP 
address, and lastly your netmask. I was able to find all of this through my travel router. In the LAN Private Network, I was given the start and end IP address, also I got the netmask and the router IP address. So I added my LAN Private Network into my Pi-hole DHCP server settings. 

Lastly, I needed to add my Pi-Hole as a client in my travel router, so I had to add my Pi to my LAN private network by putting my Pi-Hole IPV4 address and also putting the static IPV6 address of my Pi-Hole in my LAN. But then I realized that my WiFi connection from my travel router is different from my main router, so when I connected my devices to my travel router’s WiFi. Finally, I was able to see my Pi-Hole work with all of my devices across my network.

## Results

So seeing my score being a 96 out of 100 from an AdBlock tester shows that my Pi-hole works and blocks out adware, spyware, and malware queries on my network. 

<img width="833" height="348" alt="Screenshot (98)" src="https://github.com/user-attachments/assets/f348bc2f-dc0c-48d4-b66a-aa1b56d0ea47" />


These are my results after 2 hours of my Pi-hole working. I noticed that there were no more pop-up ads on sites that I would visit, and I also noticed my browsing speed has gotten faster.

<img width="1560" height="847" alt="Screenshot (86)" src="https://github.com/user-attachments/assets/63d8625d-da33-4682-bc92-5cc317a1b70f" />

Key takeaways I took from my first project were to strengthen my Linux skills and also learning about static IP, DNS, LAN, DHCP, and IP addresses. I was also able to gain hands-on experience and learn throughout this project about network security and privacy. Understanding how a Pi-hole can reduce the amount of spyware, adware, and malware queries that are happening on my network. I was finally able to deepen my skills and knowledge on how IP addresses, LAN, DHCP, DNS, and Malicious or unwanted queries play an important role in the IT and Cyber Security industry.
