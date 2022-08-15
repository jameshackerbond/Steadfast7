## Introduction
![sf7](https://user-images.githubusercontent.com/82678869/184560683-a1928028-bd59-47c6-95c2-645618b7d628.png)

Steadfast7 is a fork of Steadfast2 because The Devs of Steadfast2 have said that Steadfast2 in the near future will stop being updated once they migrate to PocketMine-MP, Steadfast7 (Name will be changed soon!) Will mainly branch off the Redstone-proxy branch for more gameplay stuff and proxy support. (Still don't know how to use it)

## Known bugs

# Normal issues:
- Players don't fall out of the world naturally, you'll want to handle PlayerMoveEvent as needed to kill them.
- When going into the void while moving when dieing can sometimes freeze the connection between the client and server.
- use-encrypt=on will crash the server for reason MCPEncrypt class not found

# Linux issues (For me)
- The console will be spammed with endless messages of an error, I will be looking into it for now use windows server or windows.
- Plugins sometimes don't work of linux, again it is another issue with linux.

IF YOU EVER NEED HELP SETTING UP STEADFAST2 OR STEADFAST7 CREATE AN ISSUE OR DM ME ON DISCORD JHB#0001 I WILL GLADLY HELP YOU.

## Notes
- Server.log will be not be saved I will implement an option to turn it off an on soon.
- If you would like to change the query motd, please build the server from source and edit src\pocketmine\network\RakLibInterface.php

## Installation

### Installing On Linux/MacOS

To install SteadyFast on Linux OS/MAC OS please follow the instructions below.

1)  do `git clone https://github.com/jameshackerbond/Steadfast7` in directory of your choosing. Or download and extract the zip into the directory of your choosing. 

2) Navigate to `Steadfast7` directory via command line

3) Run command `./installer` If successful this will create a `bin` directory with a special Php7 build in it and a `start.sh` shell script (For me it dosent generate there is a way around this by generating the phar on windows.
    
4) Running `./start` for the first time will take through the setup wizard where and create the 2 main config files for your server `pocket####mine.yml` and `server.properties`    

  *Linux VM Notes:* 
        
   - If using Vagrant have a config of `config.vm.network "public_network"` in the `Vagrantfile` should make your server discoverable from LAN. 

### Installing on Windows

Steadfast7 is not the best suited for running on Windows and another fork of Pocketmine would be better for that. But don't worry steadfast7 will still run on Windows OS with some lack of performance,

To install Steadfast7 on Windows OS please follow the instructions below.

1) To install Steadfast7 on windows OS, first you need to download the PocketMine PHP7 installer -> [from here](https://github.com/NotPocketMine/Windows-PocketMine-MP/) "Always take caution when downloading binaries off the internet" :)

2) Next, you need to run the PocketMine installer then follow the instructions provide in the installer. 

3) Then you need to navigate to your user's documents file, and delete PocketMine-MP.phar.

4) Finally, you need to move Steadfast2.phar into the directory above and run start.cmd.

We suggest a Linux VM in the meantime.  We also suggest using Vagrant and picking a Ubuntu box -> [from here](https://atlas.hashicorp.com/boxes/search?utf8=%E2%9C%93&sort=&provider=&q=ubuntu)
   
## Most Commonly Asked Questions

### Starting/Stopping Server On Windows

1) To start the server navigate to your user's documents file, and click start.cmd
2) To stop the server navigate to your user's documents file, and close the start.cmd windows

### Starting/Stopping Server On Linux/Mac

 1) To start the server open a terminal window in the server root directory and then run command `./start`.
 2) To stop the server type `stop` in the terminal of the running server. (or CTRL + C should work).  
 
## Creating the Steadfast7.phar File

To build the Steadfast7 server phar file please follow the instructions below.

1) Download the Steadfast7 master from GitHub, then unzip the master then move the src folder into your server directory, then deleted the old .phar file if you still have it in the server directory. 

2) Download the [PocketMine DevTools Plugin](https://poggit.pmmp.io/p/DevTools/1.12.1) then move the plugin into your server directory plugins folder.

3) Start the server if you don't know how to start the server follow your Starting/Stopping Server instructions above.

4) Then run makeserver in the server terminal, then it will drop the phar file in its plugin directory.
