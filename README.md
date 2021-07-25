# Optimized Spigot
"Optimized Spigot" is NOT a replacement for Spigot, PaperSpigot etc. This resource contains files that optimizes spigot to run better. The standard Spigot server configs are not that well optimized.

This resource does NOT contain a server JAR. ONLY the optimizations for a Spigot / PaperSpigot server.

I found a great thread here on SpigotMC about optimizing Spigot, so I went through it and set the values for you. You no longer need to do the work to optimize it.

This resource was configured for PaperSpigot 1.17.1, but should work for older and newer releases as well unless the files changes extensively.


INSTALLATION GUIDE
- Download the ZIP file from the Github resource
- Drop the files in the ZIP file into the server folder (if you do not run Paper, ignore "paper.yml")
- Open "bukkit.yml" and change "ServerName" to your servername (eg. HyPixel)

STARTING THE SERVER
I have added 2 startup scripts. One for Windows and one for Linux. The Windows version is the "start.bat" file. It also has a "auto-restart" implementation so that if the server crashes, it will restart by itself.
The "start.sh" file is for Linux users. This start file does NOT contain any auto-restart function. If you are a Linux user, you probably already know how to add a auto-restart function.

The scripts has the Aikar Startup Parameters set in it as well.

To start the server, you need to open the startup script in question and change 2 things:
- Max RAM
- Startup JAR file
- Startup script name (Windows only)
To change these values, edit the parameters "-Xmx4096M" and "-jar server.jar ".

Set "-Xmx4096M" to the amount of RAM that you want to allocate. This has to be in MB. So if you want to allocate, lets say 6GB RAM, you enter "-Xmx6144M".

To set the server startup JAR file, edit the "-jar server.jar" to say "-jar YOURJAR.jar" where "YOURJAR" is the name of the JAR file that you use (eg. paper.jar).

When you edited these parameters, go ahead and launch the server from the startup script and let the magic happen.

NOTE!!!!
If you are running a server with 12GB RAM or higher, you need to do some more edits.
Open the startup script and set these values

-XX:G1NewSizePercent=40
-XX:G1MaxNewSizePercent=50
-XX:G1HeapRegionSize=16M
-XX:G1ReservePercent=15
-XX:InitiatingHeapOccupancyPercent=20

To set the Startup script name (windows only), simply edit the "start.bat" file and edit "ServerName" to your servers name.
