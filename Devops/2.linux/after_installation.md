# update and upgrade
```
 sudo apt update -y; sudo apt upgrade -y;

 sudo apt install software-properties-common apt-transport-https wget

wget -qO- https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -

```

# Some installtion
```
sudo apt install vlc gimp gparted snap
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

Install Firefox .deb package for Debian-based distributions (recommended)

To install the .deb package through the APT repository, do the following:

Create a directory to store APT repository keys if it doesn't exist:
```
sudo install -d -m 0755 /etc/apt/keyrings
```
Import the Mozilla APT repository signing key:
```
wget -q https://packages.mozilla.org/apt/repo-signing-key.gpg -O- | sudo tee /etc/apt/keyrings/packages.mozilla.org.asc > /dev/null

```
If you do not have wget installed, you can install it with: 

```sudo apt-get install wget```

The fingerprint should be 35BAA0B33E9EB396F59CA838C0BA5CE6DC6315A3. You may check it with the following command:

```
gpg -n -q --import --import-options import-show /etc/apt/keyrings/packages.mozilla.org.asc | awk '/pub/{getline; gsub(/^ +| +$/,""); if($0 == "35BAA0B33E9EB396F59CA838C0BA5CE6DC6315A3") print "\nThe key fingerprint matches ("$0").\n"; else print "\nVerification failed: the fingerprint ("$0") does not match the expected one.\n"}'
```

Next, add the Mozilla APT repository to your sources.list:
    For Debian Bookworm and Older: 
```
echo "deb [signed-by=/etc/apt/keyrings/packages.mozilla.org.asc] https://packages.mozilla.org/apt mozilla main" | sudo tee -a /etc/apt/sources.list.d/mozilla.list > /dev/null
```

Configure APT to prioritize packages from the Mozilla repository:
```
echo '
Package: *
Pin: origin packages.mozilla.org
Pin-Priority: 1000
' | sudo tee /etc/apt/preferences.d/mozilla

Update your package list, and install firefox (or one of firefox-esr, -beta, -nightly, -devedition):
```
```
sudo apt-get update && sudo apt-get install firefox
```



# Git
```
sudo apt install git-all -y
```

# Vscode
## Download then run
```
sudo dpkg -i --force-all code_1.104.3-1759409451_amd64.deb
```
