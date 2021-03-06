# Valheim Server Management

This quick guide details *one way* to run a dedicated Valheim server.

First, you need to [download SteamCMD](https://developer.valvesoftware.com/wiki/SteamCMD) and open it.  

Next, log in to the Steam Public API

```
login anonymous
```

and grab the Valheim server (this is also used to update Valheim)

```bash
app_update 896660 validate
```

then exit SteamCMD

```bash
exit
```

The `Valheim/worlds` folder contains our server information.  Typically I will make a junction between this version controlled `Valheim` folder and the save location on my machine, which looks something like this:

```
mklink /J C:\Users\<USERNAME>\AppData\LocalLow\IronGate\Valheim "C:\Users\<USERNAME>\dev\valheim\Valheim
```

This allows me to quit a normal Valheim play session and simply run the following to backup my progress:

```
git add .
git commit -m "descriptive commit message about what I'm backing up"
git push
```

You can then grab any commit you want and pick up where it left off.

If you wish to rename the world saves you can use [this website](https://geekstrom.de/valheim/fwl/). Simply renaming the file is not enough.  Similarly, if you wish to rename a character, you can use [this website](https://geekstrom.de/valheim/fch/).

To start the server, run `C:\Users\<USERNAME>\Desktop\steamcmd\steamapps\common\Valheim dedicated server\valheim_server.bat` after setting the server name `-name` and password `-password` appropriately. If you are interested in running multiple servers or simply want multiple scripts for running a server in different ways and with different names, I suggest copying the `valheim_server.bat` file and modifying/renaming it appropriately. I also make shortcuts so that I don't have to dig through my steamcmd folder.