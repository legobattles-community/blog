+++
title = 'How to Setup Lego Battles Online'
date = 2024-05-30T14:37:53-04:00
draft = false
+++

Hello I'm lnee I have been doing some cursed stuff in with Linux, web hosting, and in this case Lego battles.

## Prerequisites
- A computer with Ubuntu server install on it.
- Docker to be installed on that server.
##### &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Note I use the docker deb not the snap I have not tested if the snap work*
- Access to your router console and the ability to forward port 443

## Step 1 install Kasm docker
Kasm docker is a package of Kasm web that makes think so much easier. [Kasm docker GitHub page](https://github.com/linuxserver/docker-kasm) You can find more info there about setup.

To install Kasm docker, run on the server
```
docker run -d \
  --name=kasm \
  --privileged \
  -e KASM_PORT=443 \
  -p 3000:3000 \
  -p 443:443 \
  -v /opt/kasm/data:/opt \
  -v /opt/kasm/profiles:/profiles `#optional` \
  -v /dev/input:/dev/input `#optional` \
  -v /run/udev/data:/run/udev/data `#optional` \
  --restart unless-stopped \
  lscr.io/linuxserver/kasm:latest
  ```

## Setup kasm docker

1. We need to find the local IP for your server. [Here is how.](https://linuxize.com/post/how-to-find-ip-address-linux/).

2. Once you found your server's IP in a web browser go to https://`your_ip`:3000/

3. Then in the setup ui select `ubuntu24.04 openbox` and do what it says including entering your password in

4. Forward your server's port 443 in your router console

5. Go to https://`your_ip`:443/ and login as `admin@kasm.local`

## Set up the container

1. In the top left there is a `workspaces` button, click it
![1.png](https://lneeweb.duckdns.org/images/1.png)
2. Click on `ubuntu24.04 openbox`
![2.png](https://lneeweb.duckdns.org/images/2.png)
3. Click on launch session
![3.png](https://lneeweb.duckdns.org/images/3.png)
4. Once the session launches in the sidebar, put this text in the clipboard `eval "$(curl -s "https://raw.githubusercontent.com/lnee94/resh/main/l/bsscript")"`
![1.png](https://lneeweb.duckdns.org/images/4.png)
5. Right-click on the desktop and click on open terminal.
![1.png](https://lneeweb.duckdns.org/images/5.png)
6. In the terminal, press `Ctrl+Shift+V` and press enter.
![1.png](https://lneeweb.duckdns.org/images/6.png)
7. Wait for that to finish.
![1.png](https://lneeweb.duckdns.org/images/7.png)
8. In a new tab open https://`your_ip`:443/
![1.png](https://lneeweb.duckdns.org/images/8.png)
9. Click on sessions. And in the sub bar click on sessions.
![1.png](https://lneeweb.duckdns.org/images/9.png)
10. You should see the running session. Click on the edit button of that session and the snapshot  button. Click create snapshot and your done.


