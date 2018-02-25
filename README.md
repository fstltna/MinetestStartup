# Lugdunon Startup Scripts (2.0.0)
Startup scripts for the Lugdunon MMORPG software - uses the "screen" command to manage session. This also restarts the Lugdunon process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/LugdunonStartup) - [Official Forum](https://LugdunonCity.org/index.php/forum/startup-scripts)  - [Official Download Area](https://LugdunonCity.org/index.php/downloads-new/category/14-startup-scripts)
![Lugdunon Sample Screen](https://LugdunonCity.org/lugdunon_sample_screen.png) 

---
These start up the Lugdunon server at boot time with a "screen" process.

1. Copy **lugdunon** into **/etc/init.d** - make sure it is executable
2. Copy **run.sh** into **/root/lugdunon** - make sure it is executable
3. Copy **startlugdunon** into **/root/lugdunon** - make sure it is executable
4. Run "**systemctl enable lugdunon**" (only needed once, will stick)
5. Run "**systemctl start lugdunon**" - starts Lugdunon without restarting the server

When you want to view the Lugdunon console, just enter "**screen -r**" in your shell.

To disconnect from the Lugdunon console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /root/lugdunon/nostart**". To reenable it type "**rm /root/lugdunon/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
