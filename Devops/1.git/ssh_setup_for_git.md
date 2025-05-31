# Check for existing SSH keys
```
ls -al ~/.ssh
```

# Generate a new SSH key (if none exists)

```
ssh-keygen -t ed25519 -C "saifur.rahman1193@gmail.com"

SHA256:DCPbR1+LYAH31X8849jmso+MQv9nMUD6dvwszllnmt4 saifur.rahman1193@gmail.com
```


# Start agent
```
eval "$(ssh-agent -s)"
```

# Add key
```
ssh-add ~/.ssh/id_ed25519
```

# your public key 
```
cat ~/.ssh/id_ed25519.pub

ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIJpMKGYYSYObUVFBf+X4nJC67WKhXrdvxYLAurL9taRa saifur.rahman1193@gmail.com

```

# Add SSH key to GitHub / GitLab / Bitbucket

    Go to your profile → Settings → SSH and GPG Keys

    Click “New SSH Key”

    Paste the copied key and save

```
https://github.com/settings/keys
```
