# systemd-ngrok

This utility, among other things, allows you to setup a persistent tunnel to a host system that is accessible over the web. 

## Basic persistent ssh setup

1. Create an account on https://ngrok.com
2. Download ngrok on the system that you want to tunnel into (Note: there are different versions of ngrok depending on your architecture)
3. `sudo mkdir /opt/ngrok && cp <unzipped_folder>/ngrok /opt/ngrok/`
4. Copy your authtoken from https://dashboard.ngrok.com/get-started/your-authtoken and replace it in https://github.com/ntnu-arl/systemd-ngrok/blob/edcc59014fac622a1fbbb2fbec1171ca34bf8ea1/ngrok.yml#L1
5. `sudo cp ngrok.yml /opt/ngrok/`
6. `sudo cp ngrok.service /lib/systemd/system/`
7. `systemctl enable ngrok.service && systemctl start ngrok.service`


Todo: 
check install file
