## Game Log Server

The game log server provides a way to remotely host your server's log over a http rest-ful api. 
This feature is useful if you plan on running IW4MAdmin on a different machine than the game server.

## Requirements
- [Python 3.9.x](https://www.python.org/downloads/) or newer

## Installing
1. With Python 3.9.x installed, open up a terminal/command prompt window in the `GameLogServer` folder and execute:
    ```console
    pip install -r requirements.txt
    ```
    If this fails, you can alternatively try installing with:
    ```console
    python -m pip install -r requirements.txt
    ```
2. Allow TCP port 1625 through firewall  
    * [Windows Instructions](https://www.tomshardware.com/news/how-to-open-firewall-ports-in-windows-10,36451.html)
    * [Linux Instructions (iptables)](https://www.digitalocean.com/community/tutorials/how-to-set-up-a-basic-iptables-firewall-on-centos-6#open-up-ports-for-selected-services)

## Launching  
With Python 3 installed, open a terminal/command prompt window open in the `GameServerLog`  folder and execute:
```console
python runserver.py
```
The Game Log Server window will need to remain running/open as long as **IW4MAdmin** is running

## Configuring
* Update your `IW4MAdminSettings.json` by changing the value of `GameLogServerUrl` to "http://<remote_server_ip>:1625"
* Example &mdash; `"GameLogServerUrl": "http://192.168.1.123:1625",`