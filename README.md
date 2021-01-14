# rt-ubuntu-dell-xps13-9310

* adventures in making ubuntu work for me on a dell xps 13 9310
* lots of this stuff will probably be an edge case because i migrated from WSL on a surface book 2, see https://github.com/rtanglao/rt-making-wsl-and-windows-work-for-me/blob/master/README.md

## 13janauary2020 getting ssh to work


* I googled "No more authentication methods to try." and found the 
answer here: https://askubuntu.com/questions/343060/no-more-authentication-methods-to-try-permission-denied-publickey
  * Perhaps I messed up and this isn't necessary or it's only necessary because i copied the `.ssh` directory from WSL on a surface book 2?

```
sudo chmod 700 ~/.ssh/
sudo chmod 600 ~/.ssh/*
sudo chown -R User ~/.ssh/
sudo chgrp -R User ~/.ssh/
sudo chmod 700 ~/.ssh/controlmaster

where User===roland in my case
```
