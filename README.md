```markdown
# Minecraft Server Hosting Panel with PUFFER PANEL

This guide will help you set up a Minecraft server hosting panel using PUFFER PANEL on Ubuntu VPS or Azure VPS.

## Step 1: Create a new Virtual Machine on Azure

1. Go to Azure and create a new Virtual Machine.
2. Create a Resource group if you don't have one.
3. Set the Virtual Machine Name, image to Ubuntu Server, size to max size, and authentication type to Password.
4. Set Username, Password, and Confirm password.
5. Click on Review + Create.

   ![Step 1 Screenshot 1](https://media.discordapp.net/attachments/834281126494470206/1177543152442286090/IMG_20231124_151056.jpg?ex=6572e385&is=65606e85&hm=8046a054fb1f102881869ad86e9da621159246ff414cb72d8f63df79ddc686fd&)
   ![Step 1 Screenshot 2](https://media.discordapp.net/attachments/834281126494470206/1177543152689758308/IMG_20231124_151142.jpg?ex=6572e385&is=65606e85&hm=f005416361e64b9c480973ba4b4c835ec03bc5eb95d14b287e95c00879556035&)
   ![Step 1 Screenshot 3](https://media.discordapp.net/attachments/834281126494470206/1177543153071427654/IMG_20231124_151303.jpg?ex=6572e385&is=65606e85&hm=51aff445e62fdf5ed046cbc7a2687d0c96e4d08aa536e4e6dc19b7241a2a712a&)
   ![Step 1 Screenshot 4](https://media.discordapp.net/attachments/834281126494470206/1177543153331478548/IMG_20231124_151353.jpg?ex=6572e385&is=65606e85&hm=a82feaf9cc16ec8f0ba3fd901bd1fa60534c9291ea6bdaec574978c8ca2fffaf&)
   ![Step 1 Screenshot 5](https://media.discordapp.net/attachments/834281126494470206/1177543153562173450/IMG_20231124_151438.jpg?ex=6572e385&is=65606e85&hm=004c6469fd4b3508616c51980d91bdcb5acb7a083421c4affffa917396661e5b&)
   ![Step 1 Screenshot 6](https://media.discordapp.net/attachments/834281126494470206/1177543153788653568/IMG_20231124_151517.jpg?ex=6572e385&is=65606e85&hm=e2f777cac45647ac81ca6e3cb1d864b7116ab01f524504b0d4df17a996a05db1&)
   ![Step 1 Screenshot 7](https://media.discordapp.net/attachments/834281126494470206/1177543154132590622/IMG_20231124_151624.jpg?ex=6572e385&is=65606e85&hm=10a454ccc87f8608b1123c95831d21f150253eab0c59e3a673413327b51f019a&)
   ![Step 1 Screenshot 8](https://media.discordapp.net/attachments/834281126494470206/1177543154380062762/IMG_20231124_151700.jpg?ex=6572e385&is=65606e85&hm=d5dff371ff9203681c1bb591f4a11a14b904e3f0027ea8253c4f1a25582bd372&)
   ![Step 1 Screenshot 9](https://media.discordapp.net/attachments/834281126494470206/1177543154627514428/IMG_20231124_151730.jpg?ex=6572e385&is=65606e85&hm=8f99911eccf506957d99d8fc0f8f9c83af10077fc349bf3676059f671d87675d&)
   ![Step 1 Screenshot 10](https://media.discordapp.net/attachments/834281126494470206/1177543154837233665/IMG_20231124_151815.jpg?ex=6572e385&is=65606e85&hm=ac973622486e2ca8263a624741cf23b8567dfac8868d53c53c035d93ec5c7555&)
   ![Step 1 Screenshot 11](https://media.discordapp.net/attachments/834281126494470206/1177543245048320030/IMG_20231124_151916.jpg?ex=6572e39b&is=65606e9b&hm=aa02ccf179d137f0f5bb15a5afb64986fa18e065af4ca397a0c8c772a2dbb4db&)
   ![Step 1 Screenshot 12](https://media.discordapp.net/attachments/834281126494470206/1177553019307556865/IMG_20231124_152000.jpg?ex=6572ecb5&is=656077b5&hm=3f47d1a7c5431a9145bdf2625ef3255926232f07d48ddc84a00df475c579e406&)

## Step 2: Connect to your VPS

1. Copy the VPS IP.
2. Install PuTTY to connect to the VPS using the default port 22.
3. Log in using the provided Username and Password.

   ![Step 2 Screenshot](https://media.discordapp.net/attachments/834281126494470206/1177553019307556865/IMG_20231124_152000.jpg?ex=6572ecb5&is=656077b5&hm=3f47d1a7c5431a9145bdf2625ef3255926232f07d48ddc84a00df475c579e406&)

## Step 3: Configure Inbound Port Rules

1. Go to your VPS Networking.
2. Click on Add inbound port rules.
3. Set Destination port ranges to 8080.

   ![Step 3 Screenshot 1](https://media.discordapp.net/attachments/834281126494470206/1177543245702647828/IMG_20231124_152114.jpg?ex=6572e39b&is=65606e9b&hm=9f0e52c1de97b4607cec9e706026526d5e9e3bbc04cecdf2788c86fff4a078f9&)
   ![Step 3 Screenshot 2](https://media.discordapp.net/attachments/834281126494470206/1177543246050758666/IMG_20231124_152147.jpg?ex=6572e39b&is=65606e9b&hm=b15127d476bd3b94862dd1490a8b6c1040ab451ece5b29950b27b3baac4b1a4f&)

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

   ![Step 7 Screenshot](https://media.discordapp.net/attachments/834281126494470206/1177555591909101608/Screenshot_2023-11-24-16-24-11-20_40deb401b9ffe8e1df2f1cc5ba480b12.jpg?ex=6572ef1b&is=65607a1b&hm=124f334401c89b5e5d0036c33d81fe332a8907c4567c374dbec303ac2e21d72c&)

## Step 8: Run your Minecraft server

```bash
screen -r playit.gg
```

Now, your Minecraft server hosting panel with PUFFER PANEL should be up and running. Enjoy hosting your Minecraft server!
```
