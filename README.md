# Setup Guide For GitHub

## Setup  1 Download the software GPG key generator 
[GPG Key Generator](https://www.gpg4win.org/) 

## Generate The GPG Key

```
gpg --full-generate-key
```

## List GPG Key with key IDs
```
gpg --list-secret-keys --keyid-format LONG
```
then get the id of keys 

## Export your public key
```
gpg --armor --export YOUR-KEY-ID 
```
# Add GPG key to Github account

## Configure Git on windows 
```
git config --global user.name "YOUR-NAME"
git config --global user.email "YOUR-EMAIL"
git config --global user.signingkey YOUR-KEY-ID 
git config --global commit.gpgsign true
git config --global tag.gpgsign true
git config --global gpg.program "C:\Program Files (x86)\GnuPG\bin\gpg.exe"
```

## List global git config 
```
git config --global --list
```
[Youtube Video](https://youtube.com/watch?v=xj9OiJL56pM&t=473s)

## Signed commit  