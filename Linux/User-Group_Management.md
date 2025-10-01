# 👤 User & Group Management in Linux

## Basic Commands

### ➡️ Add a new user
```bash
sudo useradd <username>
```


### ➡️ Add user with Home directory
```bash
sudo useradd -m <username>
```


### ➡️ Set password for user
```bash
sudo passwd <username>
```


### ➡️ Delete a user
```bash
sudo userdel <username>
```


### ➡️ Delete a user with home directory
```bash
sudo userdel -r <username>
```

## Medium Commands

### ➡️ Add user to group
```bash
sudo usermod -aG <groupname> <username>
```


### ➡️ Show group user belong to
```bash
groups <username>
```


### ➡️ Create a new group
```bash
sudo groupadd <groupname>
```


### ➡️ Add user to that group
```bash
sudo usermod -aG <groupname> <username>
```


### ➡️ Change user's default Shell
```bash
sudo usermod -s /bin/bash <username>
```


### ➡️ Lock a user account
```bash
sudo usermod -L <username>
```


### ➡️ Unlock a user account
```bash
sudo usermod -U <username>
```

## Advanced Commands

### ➡️ Check last login info
```bash
lastlog | grep <username>
```


### ➡️ switch to another account
```bash
su - <username>
```
note-> su <username> a quick commands without changin uur environment as above command the environment


### ➡️ Force password change for at next login
```bash
sudo change -d  0 <username>
```


### ➡️ View password expiry details
```bash
sudo chage -l devuser
```


### ➡️ Delete a group
```bash
sudo groupdel devops
```
