# ssh_authentication

## Tonton Jo  
### Join the community:
[![Youtube channel](https://github-readme-youtube-stats.herokuapp.com/subscribers/index.php?id=UCnED3K6K5FDUp-x_8rwpsZw&key=AIzaSyA3ivqywNPQz0xFZBHfPDKzh1jFH5qGD_g)](http://youtube.com/channel/UCnED3K6K5FDUp-x_8rwpsZw?sub_confirmation=1)
[![Discord Tonton Jo](https://badgen.net/discord/members/h6UcpwfGuJ?label=Discord%20Tonton%20Jo%20&icon=discord)](https://discord.gg/h6UcpwfGuJ)
### Support the channel with one of the following link:
[![Ko-Fi](https://badgen.net/badge/Buy%20me%20a%20Coffee/Link?icon=buymeacoffee)](https://ko-fi.com/tontonjo)
[![Infomaniak](https://badgen.net/badge/Infomaniak/Affiliated%20link?icon=K)](https://www.infomaniak.com/goto/fr/home?utm_term=6151f412daf35)
[![Express VPN](https://badgen.net/badge/Express%20VPN/Affiliated%20link?icon=K)](https://www.xvuslink.com/?a_fid=TontonJo)  

## Usage:
### Generate a pair of rsa keys in the folder of your choice
```shell
ssh-keygen -t rsa -b 4096 -C "name of user"
```
- Alternatively, specifiy output path directly in command
```shell
ssh-keygen -t rsa -b 4096 -C "name of user" -f /root/user_rsa
```

### Deploy your public key on the servers you want to connect using private key
```shell
ssh-copy-id -i "/root/user_rsa.pub" root@127.0.0.1
```
### In case of need, you can specify the port of the remote server
```shell
ssh-copy-id -i "/root/user_rsa.pub" -p 22 root@10.0.0.41
```

## Disable password login for root
```shell
nano /etc/ssh/sshd_config
```
- set
PermitRootLogin prohibit-password
