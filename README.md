# GOAD Ultra-Light

This repo is entirely based on https://github.com/Orange-Cyberdefense/GOAD
All credits goes back to them !

I only did minor changes to get an UltraLight version for computers with very limited capacity.

## Installation (checked on Kali)

```
sudo apt-get install -y virtualbox vagrant docker.io
sudo vagrant plugin install winrm
sudo vagrant plugin install winrm-elevated
sudo vagrant plugin install winrm-fs

sudo ./goad.sh -t check -l GOAD-UltraLight -p virtualbox -m docker
sudo ./goad.sh -t install -l GOAD-UltraLight -p virtualbox -m docker
```

## Changes (relative to the Light version)

  * 2 GB RAM instead of 4
  * Removed DC01 : only 1 domain (north.sevenkingdoms.local) with 2 servers
  * Removes IIS and mssql installation (this lab only demonstrated classic Kerberos and NTLM vulns)
  * Changed the timing of responder and ntlmrelay (1 instead of 3 and 5 minutes)


# Note

I would like to extend my most sincere gratitude to mayfly for this amayzing piece of work !

Check out the solution on his blog : https://mayfly277.github.io/posts/GOADv2/
