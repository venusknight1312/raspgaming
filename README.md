# raspgaming

#THIS CODING IS FOR THE RASPBERRY PI GAMING CONSOLE 

#YOU WILL NEED TO FOLLOW THE STEPS AS IT IS 

#IF YOU LAND INTO SOME PROBLEMS THEN CONCTACT ME ON VENUSKNIGHT1312@GMAIL.COM

Once Raspbian is up and running we have only a few minor things to attend to before we can start playing our games. Before we dive into all the commands we would strongly encourage you to configure your Pi to accept an SSH connection so that you can enter all of these commands from the comfort of your main computer (and with the comfort of cut and paste at that).

The first step is to add Moonlight to your Pi’s repository list so we can use the apt-get command to pull down the packages instead of fussing with getting the full file URLs from the Moonlight GitHub repository and manually installing it.

Enter the following command while logged in as the root user on your Pi (the default is username “pi” password “raspberry”).

sudo nano /etc/apt/sources.list

This will open up your repository sources list. Add the following line to the list.

deb http://archive.itimmer.nl/raspbian/moonlight wheezy main


Exit nano by pressing CTRL+X, save the document when prompted. Next, we’ll install Moonlight. Enter the following commands.

apt-get update
apt-get install moonlight-embedded

When prompted answer all the questions “Y” to install all the necessary files.

This is the process we used and it should work for the vast majority of users. If for any reason you wish to manually install the Moonlight software and dependencies, please refer to the readme file for the Moonlight Embedded at GitHub here for additional information.

The final step is to pair your gaming PC to the Pi. Again at the command prompt on the Pi, enter the following command where X.X.X.X is the local network IP address of the gaming PC.


moonlight pair X.X.X.X



The command will generate a certificate and a four digit PIN.

Enter the PIN to complete the pairing process and authorize the Moonlight/Pi unit to access your game stream.








