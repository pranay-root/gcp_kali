# gcp_kali

Create a new instance with 30 gb ssd and debian 11 amd bullseye 
then use the below commands one by one (last updated 07th May 2024)
```
sudo su
apt update
nano /etc/apt/sources.list (remove any exisiting text in that )
```
add this ```deb http://http.kali.org/kali kali-last-snapshot main contrib non-free non-free-firmware``` and save the file.
```
apt update
gpg --keyserver keyserver.ubuntu.com --recv-key ED444FF07D8D0BF6
gpg -a --export ED444FF07D8D0BF6 > /tmp/key.asc
sudo cp /tmp/key.asc /etc/apt/trusted.gpg.d/
sudo apt update
sudo apt full-upgrade -y 
sudo apt install -y kali-linux-default
```
The whole process can take upto an hour so wait till its done use mobile hotspot if you have issue with wifi or power cut problems.
Once it is done the kali linux will be installed with every tool check the last updated comment to get the latest version.
Thank you
