1. Go to Azure and create a new Virtual Machine.
2. Create a Resource group if you don't have one. Set the Virtual Machine Name, image to Ubuntu Server, size to max size, and in Authentication type to Password. Then, set Username, Password, Confirm password. Don't click on select inbound ports; then, click on Review + Create.
https://cdn.discordapp.com/attachments/834281126494470206/1177543152442286090/IMG_20231124_151056.jpg?ex=6572e385&is=65606e85&hm=8046a054fb1f102881869ad86e9da621159246ff414cb72d8f63df79ddc686fd&
https://cdn.discordapp.com/attachments/834281126494470206/1177543152689758308/IMG_20231124_151142.jpg?ex=6572e385&is=65606e85&hm=f005416361e64b9c480973ba4b4c835ec03bc5eb95d14b287e95c00879556035&
https://cdn.discordapp.com/attachments/834281126494470206/1177543153071427654/IMG_20231124_151303.jpg?ex=6572e385&is=65606e85&hm=51aff445e62fdf5ed046cbc7a2687d0c96e4d08aa536e4e6dc19b7241a2a712a&
https://cdn.discordapp.com/attachments/834281126494470206/1177543153331478548/IMG_20231124_151353.jpg?ex=6572e385&is=65606e85&hm=a82feaf9cc16ec8f0ba3fd901bd1fa60534c9291ea6bdaec574978c8ca2fffaf&
https://cdn.discordapp.com/attachments/834281126494470206/1177543153562173450/IMG_20231124_151438.jpg?ex=6572e385&is=65606e85&hm=004c6469fd4b3508616c51980d91bdcb5acb7a083421c4affffa917396661e5b&
https://cdn.discordapp.com/attachments/834281126494470206/1177543153788653568/IMG_20231124_151517.jpg?ex=6572e385&is=65606e85&hm=e2f777cac45647ac81ca6e3cb1d864b7116ab01f524504b0d4df17a996a05db1&
https://cdn.discordapp.com/attachments/834281126494470206/1177543154132590622/IMG_20231124_151624.jpg?ex=6572e385&is=65606e85&hm=10a454ccc87f8608b1123c95831d21f150253eab0c59e3a673413327b51f019a&
https://cdn.discordapp.com/attachments/834281126494470206/1177543154380062762/IMG_20231124_151700.jpg?ex=6572e385&is=65606e85&hm=d5dff371ff9203681c1bb591f4a11a14b904e3f0027ea8253c4f1a25582bd372&
https://cdn.discordapp.com/attachments/834281126494470206/1177543154627514428/IMG_20231124_151730.jpg?ex=6572e385&is=65606e85&hm=8f99911eccf506957d99d8fc0f8f9c83af10077fc349bf3676059f671d87675d&
https://cdn.discordapp.com/attachments/834281126494470206/1177543154837233665/IMG_20231124_151815.jpg?ex=6572e385&is=65606e85&hm=ac973622486e2ca8263a624741cf23b8567dfac8868d53c53c035d93ec5c7555&
https://cdn.discordapp.com/attachments/834281126494470206/1177543245048320030/IMG_20231124_151916.jpg?ex=6572e39b&is=65606e9b&hm=aa02ccf179d137f0f5bb15a5afb64986fa18e065af4ca397a0c8c772a2dbb4db&

3. Go to your VPS, copy the VPS IP, and install PuTTY to connect to the VPS. Your VPS default port is 22; don't change it. Log in using Username and Password.
https://cdn.discordapp.com/attachments/834281126494470206/1177543245333540874/IMG_20231124_152037.jpg?ex=6572e39b&is=65606e9b&hm=81e0d28942dd6b12b969ed77c020386a8a87fb4cb0e34573659c665a8f4de5d7&
4. Go to your VPS Networking, click on Add inbound port rules, then set Destination port ranges to 8080.
https://cdn.discordapp.com/attachments/834281126494470206/1177543245702647828/IMG_20231124_152114.jpg?ex=6572e39b&is=65606e9b&hm=9f0e52c1de97b4607cec9e706026526d5e9e3bbc04cecdf2788c86fff4a078f9&
https://cdn.discordapp.com/attachments/834281126494470206/1177543246050758666/IMG_20231124_152147.jpg?ex=6572e39b&is=65606e9b&hm=b15127d476bd3b94862dd1490a8b6c1040ab451ece5b29950b27b3baac4b1a4f&
https://cdn.discordapp.com/attachments/834281126494470206/1177543246315016262/IMG_20231124_152232.jpg?ex=6572e39b&is=65606e9b&hm=e81bfa4a0dacd640d9e53b2d91684c87c01d3d25960515842ed40a8a4c384392&
https://cdn.discordapp.com/attachments/834281126494470206/1177543246545686548/IMG_20231124_152325.jpg?ex=6572e39b&is=65606e9b&hm=2242ea958803414373abe61397fb96651923d22558424913126c9e562a49be23&
5. Run the following commands in sequence:
    bash
    sudo -s
    apt update && apt upgrade && apt install curl && apt install systemctl && apt install docker && sudo apt install playit
    
6. Run the following command to install PufferPanel:
    bash
    curl -s https://packagecloud.io/install/repositories/pufferpanel/pufferpanel/script.deb.sh | sudo bash
    
7. Install PufferPanel:
    bash
    apt-get install pufferpanel
    
8. Enable PufferPanel:
    bash
    systemctl enable pufferpanel
    
9. Start PufferPanel:
    bash
    systemctl start pufferpanel
    
10. Add a user to PufferPanel:
    bash
    pufferpanel user add
    
11. Open Chrome and navigate to http://your-vps-ip:8080/.
https://cdn.discordapp.com/attachments/834281126494470206/1177543245333540874/IMG_20231124_152037.jpg?ex=6572e39b&is=65606e9b&hm=81e0d28942dd6b12b969ed77c020386a8a87fb4cb0e34573659c665a8f4de5d7&

12. Now run ```screen -r playit.gg```
