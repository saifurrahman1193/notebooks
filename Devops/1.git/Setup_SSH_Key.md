# Solution: Set Up SSH Key Authentication
```
ssh-keygen -t ed25519 -C "saifur.rahman@gmail.com"
```

# Copy key
```
cat ~/.ssh/id_ed25519.pub
```

### Go to GitHub → Settings → SSH and GPG Keys → New SSH Key and paste it.
```
ssh-ed25519 AAAACafassadas1lZDI1NTE5AAAAIL4rXasdsadRWy6CVWYBFEWDDFDHHH7S53HE saifur.rahman@gmail.com

```

## test with
```
ssh -T git@github.com
yes
```

# Clone a repository using SSH
```
git clone git@github.com:saifurrahman/wintext_ds.git
```