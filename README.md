# Valheim Server Management

- [Download SteamCMD](https://developer.valvesoftware.com/wiki/SteamCMD)

- Log in to Steam Public

```bash
login anonymous
```

- Update Valheim

```bash
app_update 896660 validate
```

- Exit SteamCMD

```bash
exit
```

The `Valheim/worlds` folder contains our server information.

To start the server, run `C:\Users\<USERNAME>\Desktop\steamcmd\steamapps\common\Valheim dedicated server\valheim_server.bat` after setting the server name `-name` and password `-password` appropriately.