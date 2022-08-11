# What is Dev Env and Benefits

## Vagrant and Virtual Box

## Steps

- Make a directory

  `mkdir new_folder`

- Move in the directory

  `cd new_folder`

- Create a Vagrant file
  `nano Vagrantfile`

- Paste the block of code and save it

```
Vagrant.configure("2") do |config|

 config.vm.box = "ubuntu/xenial64" # Linux - ubuntu 16.04
# creating a virtual machine ubuntu




end
```

- Check if the code has been pasted

  `cat Vagrantfile`

- In the same directory run the command:

  `vagrant up`

- Check the status using:

  `vagrant status`

- Start ssh

  `vagrant ssh`

### Troubleshooting:

If there is an issue with vagrantfile, use commands:

`vagrant destroy` --> say yes

`ls -a`

`rm -rf .vagrant`

`rm -rf Vagrantfile`

- Follow the steps above to create a new Vagrantfile.

## Virtualisation?

- how can we find out the name of OS
  `uname` or `uname -a`

- how to create a file in Linux
  `touch filename` or `nano filename`

- how to check existing file/folders `ls` or `ls -a`
- how to create a folder `mkdir foldername`
- how to navigate inside the folder `cd foldername`
- how to come out of the folder or 1 step back `cd ..`
- how to check our current location `pwd`
- `whoami`
- how to copy file `cp filename_with_absolute_path destination_with_absolute_path`
- how to remove file/folder `rm -rf file/folder_name`
- how to cut paste/move the file `mv filename_with_absolute_path foldername_with_absolute_path`
- how to check all processes `top` and `ps aux`
- how to use root user `sudo su` or `sudo i`
- how to use `|` pipe
- how to remove/delete/kill process
- how to check file permission `ll`
- change file permission `chmod permission filename`
  - `r` or `w` or `rw` `all` also numbers `400` or `600` for all `700`
- update our ubuntu OS `sudo apt-get update`
- upgrade or ubuntu OS `sudo apt-get upgrade` or `sudo apt-get upgrade -y`
- how to create automate tasks with provisioning scripts
- automate update and upgrade
- `sudo nano provision.sh`
- `sudo cat provision.sh`
- `sudo chmod +x provision.sh`
- run provision.sh `./provision.sh`
