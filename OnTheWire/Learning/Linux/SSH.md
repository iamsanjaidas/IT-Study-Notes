The default SSH port number is 22. So when you use `ssh user@IP`, it tries to connect to the default port 22. But if the remote server uses some other port for SSH, you should provide the port number:

```
ssh -p port_number user@IP
```

Let's say you want to connect to a remote server with IP 64.227.184.93 that accepts SSH connections at port number 7770

```
ssh -p 7770 Sanjai@64.227.184.93
```

**That was about connecting to a different port via SSH. What about changing the SSH port on your server?**

The process is simple:

- Decide which port number XXXX you want to use
- If you have an **active firewall on the server, allow the new port** XXXX
- Edit the `/etc/ssh/sshd_config` file and replace the line `#Port 22` with `Port XXXX`
- Restart the SSH service with `systemctl restart sshd`


### Step 1: Choose a port number

You can choose any port number between 0 and 65535 except the [common networking ports](https://linuxhandbook.com/common-ports/?ref=itsfoss.com) like 21, 80, 443 etc.

Can't pick. Let's say you use 7770 for the new SSH port.

Now, **log in to the server where you want to make these changes**.

### Step 2: Allow the new port through the firewall

As a sysadmin you probably know if there is a firewall active on your system or not.

Different types of distributions have different firewalls. I cannot cover all of them so that onus lies on you.

I am using Ubuntu server and there you have the UFW. [Check the UFW firewall status](https://learnubuntu.com/check-firewall-status/?ref=itsfoss.com):

```
sudo ufw status
```

If it is active, [allow the new port through the firewall](https://learnubuntu.com/allow-port-firewall/?ref=itsfoss.com):

```
sudo ufw allow 7770
```

### Step 3: Edit the ssh config file

[Use Vim or Nano](https://itsfoss.com/vim-vs-nano/) to edit the config file in the terminal. I'll use nano here:

```
nano /etc/ssh/sshd_config
```

In the file locate the line with `#Port 22`. It should be at the beginning of the file.

### Restart SSH service

Now that you have made changes to config file, [restart the service](https://itsfoss.com/start-stop-restart-services-linux/) SSH daemon.

Most distros these days use systemd and hence use this command to restart it:

```
systemctl restart sshd
```

And that's it. No need to restart the server itself.

Now when you have to connect to the server via SSH, specify the port number:

```
ssh -p xxxx user@ip
```