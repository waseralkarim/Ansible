## Passwordless Authentication

It allows us to connect to the vm, ec etc. without needing password or ssh-keys

![Image](https://github.com/user-attachments/assets/0bfe49e1-28ad-4339-8214-f3935dc89347)

There are two-way passwordless authentication works:

![Image](https://github.com/user-attachments/assets/1b66d3f9-a996-47ba-892a-0ce37b88e5c7)

# **Passwordless authentication commands:**

### **EC Instances**

```bash
ssh-copy-id -f "-o IdentityFile <PATH_TO_PEM_FILE>" ubuntu@<INSTANCE_PUBLIC_IP>
```

### **Using Password (Not recommended)**

First you need to open the console or ssh the node and follow the instructions below:

- Go to the file /etc/ssh/sshd_config.d/60-cloudimg-settings.conf
- Update PasswordAuthentication yes
- Restart SSH -> sudo systemctl restart ssh

If you are not on ec instances the location will be /etc/ssh/sshd_config.d and there will be file a field called PasswordAuthentication no. Update the field to PasswordAuthentication yes.

After that run sudo systemctl restart ssh . Additionally set password for the ubuntu user by running the command sudo passwd ubuntu
