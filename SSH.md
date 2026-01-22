# SSH  Commands

To ssh into the SERVER, your server should have the Your PUBLIC KEY and you must keep the PRIVATE KEY in your laptop
______________________________________________________________________________________________________________________________________________________________________________
The keys ,if generated will be stored in 
```bash
ls ~/.ssh
```
like 
- ~/.ssh/id_rsa
- ~/.ssh/id_rsa.pub

To generate the key use the command 

ed25519 encryption algo ( recommended )
```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```
rsa encryption algo 
```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
_________________________________________________________________________________________________________________________________________________________________________________
Copy the public key to the server 

Easiest :
```bash
ssh-copy-id user@server_ip
```
Enter the password once ,Automatically adds key to ~/.ssh/authorized_Keys

If the ssh-copy-id is not availabel :
On your laptop :
Copy the public key :
```bash
cat ~/.ssh/public-key-name.pub
```

On the server : 
```bash
mkdir -p ~/.ssh
nano ~/.ssh/authorized_keys
```
Paste the public key and save 

Fix the permissoin : 
```bash
chmod 700 ~/.ssh
chmod 600 ~/.ssh/authorized_keys
```
 Now ssh into the server : 
 ```bash
ssh username@server_ip
```
To verify use the following command 
```bash
ssh -v user@server_ip
```
You  should see something like this : 
Offering public key
Authentication succeeded

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Using Custom .pem file 

```bash
ssh -i mypemkey.pem Username@server_ip
```
Change the permisson if needed
```bash
chmod 400 mypemkey.pem
```
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Copying the file into the server :

laptop -> server
```bash
scp app.jar user@server_ip:/opt/app
```

server -> laptop
```bash
scp user@server_ip:/var/log/syslog .
```
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Running remote command:
```bash
ssh user@server_ip "command you want to execute "
```

Port forwarding :
```bash
ssh -L 8080:localhost:8080 user@server_ip
```
After this access the server locally at : 
```bash
http://localhost:8080
```
deletes the old server key from your laptop so you can connect again safely
```bash
ssh-keygen -R server_ip
```
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Editing the ssh config.files

Edit the config file :
```bash
vim ~/.ssh/config
```
Add the following details regarding the server: 
```bash
Host myserver
  HostName 13.xxx.xxx.xxx
  User ubuntu
  IdentityFile ~/.ssh/id_rsa
```
Now  connect to the server using :
```bash
ssh myserver
```

 COMMON FAILURES (and WHY) 
     Error	                          Cause
Permission denied	            Key not added / wrong user
Connection timed out	        irewall / SG
Host key verification failed	known_hosts mismatch










