# debian setup

## Prep

```
apt-get update
apt-get install sudo
```

## Set

```
vi /etc/sudoers
%USER% ALL=(ALL:ALL) ALL
```

### apt-get install

```
sudo apt-get install trash-cli git curl
```

### node

```
curl -sL https://deb.nodesource.com/setup_10.x -o nodesource_setup.sh
sudo bash nodesource_setup.sh
sudo apt install nodejs
npm i n -g
n stable
```

### code

```
curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg
sudo install -o root -g root -m 644 microsoft.gpg /etc/apt/trusted.gpg.d/
sudo sh -c 'echo "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list'

sudo apt-get install apt-transport-https
sudo apt-get update
sudo apt-get install code # or code-insiders
```

#### optional

```
sudo apt-get install screen
gnome-tweak-tool
```

#### ? Unable to lock the administration directory

```
sudo rm /var/lib/apt/lists/lock
sudo rm /var/cache/apt/archives/lock
sudo rm /var/lib/dpkg/lock
```

#### ? VM - shared folders location

```
cd /mnt/hgfs
```
