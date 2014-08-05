ZoomHash Pi Software
====================
<strong style="color: red;">Last Update: 7-24-14</strong><br /><br />
ZoomHash Pi Software is a complete solution for all your mining needs.<br />
Works with both Gridseeds and ZeusMiners<br />
Make sure your device is on for 5 seconds before starting the Pi!<br /><br />
<strong>Flashable 7-21-14 image located here: http://p.lewd.es/zeusgrid-7-21-14.img.gz<br /><br />
You will need to follow update instructions to make it 100% up to date but this will get you up and running if you are just looking for a flashable solution and not wanting to update</strong><br /><br />


<h2>How to Update your Raspberry Pi Software</h2>
You will need to login to your pi via SSH. To do this you need a program called Putty, there are many guides on how to SSH. 

```
Default username: pi
Default password: zoomhash
```


Now you will need to exectue some simple commands, just copy and paste each line and you should be OK!<br /><br />
```
cd /var/www
sudo git clone https://github.com/nvreaver/ZoomHash-Pi-Software.git
cd /var/www/ZoomHash-Pi-Software
sudo ./update.sh
```


<br />

<h2>Human Readable Changelog (7-24-14)</h2>
<ul>
<li>Added default values for frequency (highly requested) default value for Gridseed is 800, and ZeusMiner is 328<br /></li>
<li>Fixed a bug with file permission of the minerconfig.dat, nothing too pressing but was bugging me!<br/></li>
<li>Added reading from minerconfig.dat so you don't have to wait to see your settings, previously pulled from the miner directly, but I can see how this would cause people to think that their setting are not saved.<br /></li>
</ul>

<br />

<h2>Human Readable Changelog (7-23-14)</h2>
<ul>
<li>Removed unnecessary files<br /></li>
<li>Fixed a bug where the ZeusMiner frequency would always show 368 even if the value was different<br/></li>
<li>Added recommended default frequency values for ZeusMiner (328).<br /></li>
</ul>


<br />
<h2>Human Readable Changelog (7-22-14)</h2>
<ul>
<li>ZeusMiner Support<br /></li>
<li>Added BFGMiner 4.3.1 Custom (Darkwinde Fork)<br /></li>
<li>Added chip count for ZeusMiners<br /></li>
<li>Added frequency for ZeusMiners<br /></li>
<li>Added unit count for both ZeusMiners and Gridseeds<br /></li>
<li>Changed how adding pools and frequency works, hopefully no more hassle with the software sometimes not recognizing your pool information<br /></li>
<li>minerconfig.json redone as minerconfig.dat, will instead read a regular dat file instead of a json, will help with recognizing pool information<br /></li>
<li>Added restart pi option (will have to manually refresh the page after the pi is rebooted)<br /></li>
<li>Reboot after saving settings (changing pool information) page will begin refreshing once the Pi is booted up<br /></li>
<li>Squashed some bugs, no more scary errors about a socket being missing, no more division by 0<br /></li>
<li>Added checks to make sure that Gridseed and ZeusMiners are correctly adding if both or either are available<br /></li>
<li>If you desire to SSH and see the software running you can do so now, added commands to easily see both ZeusMiners and Gridseeds, help information on the left sidebar for SSH commands<br /></li>
<li>rc.local no longer handling startup, added new script so there is no more confusion by the system (sometimes wouldn't start up CPUMiner)<br /></li>
<li>No longer outputs errors if there is no miner running, will wait until pool information is added<br /></li>
<li>Removed initial pool settings (rc.local change makes it so we don't have to have default pool information any longer)<br /></li>
<li>Removed a bug some users were telling me about the pool information wiping when typing in and the page auto refreshed<br /></li>
</ul>
