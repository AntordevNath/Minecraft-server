```markdown
# Minecraft Server Hosting Panel with PUFFER PANEL

This guide will help you set up a Minecraft server hosting panel using PUFFER PANEL on Ubuntu VPS or Azure VPS.

## Step 1: Create a new Virtual Machine on Azure

1. Go to Azure and create a new Virtual Machine.
2. Create a Resource group if you don't have one.
3. Set the Virtual Machine Name, image to Ubuntu Server, size to max size, and authentication type to Password.
4. Set Username, Password, and Confirm password.
5. Click on Review + Create.
```
   ![Step 1 Screenshot 1](https://media.discordapp.net/attachments/834281126494470206/1177543152442286090/IMG_20231124_151056.jpg)
   ![Step 1 Screenshot 2](https://media.discordapp.net/attachments/834281126494470206/1177543152689758308/IMG_20231124_151142.jpg)
   ![Step 1 Screenshot 3](https://media.discordapp.net/attachments/834281126494470206/1177543153071427654/IMG_20231124_151303.jpg)
   ![Step 1 Screenshot 4](https://media.discordapp.net/attachments/834281126494470206/1177543153331478548/IMG_20231124_151353.jpg)
   ![Step 1 Screenshot 5](https://media.discordapp.net/attachments/834281126494470206/1177543153562173450/IMG_20231124_151438.jpg)
   ![Step 1 Screenshot 6](https://media.discordapp.net/attachments/834281126494470206/1177543153788653568/IMG_20231124_151517.jpg)
   ![Step 1 Screenshot 7](https://media.discordapp.net/attachments/834281126494470206/1177543154132590622/IMG_20231124_151624.jpg)
   ![Step 1 Screenshot 8](https://media.discordapp.net/attachments/834281126494470206/1177543154380062762/IMG_20231124_151700.jpg)
   ![Step 1 Screenshot 9](https://media.discordapp.net/attachments/834281126494470206/1177543154627514428/IMG_20231124_151730.jpg)
   ![Step 1 Screenshot 10](https://media.discordapp.net/attachments/834281126494470206/1177543154837233665/IMG_20231124_151815.jpg)
   ![Step 1 Screenshot 11](https://media.discordapp.net/attachments/834281126494470206/1177543245048320030/IMG_20231124_151916.jpg)
   ![Step 1 Screenshot 12](https://media.discordapp.net/attachments/834281126494470206/1177553019307556865/IMG_20231124_152000.jpg)
```
## Step 2: Connect to your VPS

1. Copy the VPS IP.
2. Install PuTTY to connect to the VPS using the default port 22.
3. Log in using the provided Username and Password.
```
   ![Step 2 Screenshot](https://media.discordapp.net/attachments/834281126494470206/1177553019307556865/IMG_20231124_152000.jpg)
```
## Step 3: Configure Inbound Port Rules

1. Go to your VPS Networking.
2. Click on Add inbound port rules.
3. Set Destination port ranges to 8080.
```
   ![Step 3 Screenshot 1](https://media.discordapp.net/attachments/834281126494470206/1177543245702647828/IMG_20231124_152114.jpg)
   ![Step 3 Screenshot 2](https://media.discordapp.net/attachments/834281126494470206/1177543246050758666/IMG_20231124_152147.jpg)

## Step 4: Run the following commands

```bash
sudo -s
apt update && apt upgrade && apt install curl && apt install systemctl && apt install docker && sudo apt install playit
```

## Step 5: Install PufferPanel

```bash
curl -s https://packagecloud.io/install/repositories/pufferpanel/pufferpanel/script.deb.sh | sudo bash
apt-get install pufferpanel
systemctl enable pufferpanel
systemctl start pufferpanel
```

## Step 6: Add a user to PufferPanel

```bash
pufferpanel user add
```

## Step 7: Open PufferPanel in your browser

Open Chrome and navigate to `http://your-vps-ip:8080/`.

   ![Step 7 Screenshot](https://media.discordapp.net/attachments/834281126494470206/1177555591909101608/Screenshot_2023-11-24-16-24-11-20_40deb401b9ffe8e1df2f1cc5ba480b12.jpg)

## Step 8: Run your Minecraft server

```bash
screen -r playit.gg
```

Now, your Minecraft server hosting panel with PUFFER PANEL should be up and running. Enjoy hosting your Minecraft server!
```

Replace the existing markdown with this, and the images should be displayed properly.
