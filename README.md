# hestiacp-flarum
A Quick Install App for [Hestia Control Panel](https://hestiacp.com) that allows you to easily install [Flarum](https://flarum.org), a modern, fast, open source, website forum software. 

## Requirements
A Hestia Control Panel with Apache2 support. 

## Installation
You will need to simply copy the Flarum folder to your Hestia WebApps folder at /usr/local/hestia/web/src/app/WebApp/Installers. For example, with SSH access into your server, you can run the following commands to download, unzip, move the Flarum folder into place, and set permissions:

```
cd /tmp
wget https://github.com/Steveorevo/hestiacp-flarum/archive/refs/heads/main.zip
unzip main.zip
sudo mv ./hestiacp-flarum-main/Flarum /usr/local/hestia/web/src/app/WebApp/Installers
sudo chmod 644 /usr/local/hestia/web/src/app/WebApp/Installers/Flarum/*
sudo chown -R root:root /usr/local/hestia/web/src/app/WebApp/Installers/Flarum
```

## Usage
Create a web domain in Hestia and select the Quick Install button. You should have Flarum listed as an item. Selecting it will allow you to install Flarum. By default, it will install in the root of the domain's public_html folder. However, you can easily specify a subfolder. For instance, you could have WordPress in your root and Flarum in a subfolder such as /forum (i.e. accessible at http://example.com/forum). You can even recycle your existing database credentials from WordPress as Flarum installer will automatically select a random database prefix. 

