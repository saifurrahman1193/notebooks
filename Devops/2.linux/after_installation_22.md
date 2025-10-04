# update and upgrade
```
 sudo apt update -y; sudo apt upgrade -y;

 sudo apt install software-properties-common apt-transport-https wget

wget -qO- https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -

```

# Some installtion
```
sudo apt install vlc gimp gparted snap

sudo snap install telegram-desktop
sudo snap install chromium
sudo snap install opera
sudo snap install whatsapp-desktop-client
sudo apt-get install git

```



# Swap
It looks like you already have a **2 GB swap file** enabled, but you'd like to increase it to **16 GB**. Since your current swap file is 2 GB, you'll need to create a new, larger swap file and remove the old one.

Here's how to proceed:

### 1. **Turn off the current swap file**:

To modify the current swap file, you first need to turn it off.

```bash
sudo swapoff /swapfile
```

### 2. **Remove the old swap file** (optional):

If you're replacing the current swap file, you can remove the old one:

```bash
sudo rm /swapfile
```

### 3. **Create a new swap file of 16 GB**:

Now, let's create a new swap file of **16 GB**:

```bash
sudo fallocate -l 16G /swapfile
```

If `fallocate` doesn't work or if you prefer a more reliable method, you can use `dd`:

```bash
sudo dd if=/dev/zero of=/swapfile bs=1M count=16384
```

### 4. **Set the correct permissions**:

Set the right permissions for the swap file to ensure only root can access it:

```bash
sudo chmod 600 /swapfile
```

### 5. **Format the new swap file**:

Now, format the swap file to make it usable:

```bash
sudo mkswap /swapfile
```

### 6. **Activate the new swap file**:

Enable the swap file:

```bash
sudo swapon /swapfile
```

### 7. **Make the swap permanent** (optional but recommended):

To ensure the swap is enabled on boot, add it to `/etc/fstab`.

Open `/etc/fstab` for editing:

```bash
sudo nano /etc/fstab
```

Add the following line to the end of the file:

```
/swapfile none swap sw 0 0
```

Save the file and exit (`Ctrl + X`, then `Y`, and `Enter`).

### 8. **Check the swap space**:

Finally, confirm that the new swap file is active and has the correct size:

```bash
swapon --show
```



# Firefox


```bash
sudo snap remove firefox
sudo apt remove firefox
sudo apt purge firefox
sudo apt autoremove
rm -rf ~/.mozilla
rm -rf ~/.cache/mozilla
sudo snap install firefox
```



# Git
```
sudo apt install git -y
```

# Vscode
## Download then run
```
sudo snap install code --classic
```

# sublime
```
sudo snap install sublime-text --classic

```
