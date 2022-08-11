# What is Dev Env?

A development environment is the collection of processes and tools that are used to develop the source code for a program or software product. This involves the entire environment that supports the process end to end, including development, staging and production servers

## Vagrant and Virtual Box

- Vagrant is a tool for building and managing virtual machine environments in a single workflow.
- VirtualBox is open-source software for virtualizing the x86 computing architecture.

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

## What is Virtualisation?

Virtualisation creates a simulated, or virtual, computing environment as opposed to a physical environment. Virtualisation often includes computer-generated versions of hardware, operating systems, storage devices and more. This allows organisations to partition a single physical computer or server into several virtual machines. Each virtual machine can then interact independently and run different operating systems or applications while sharing the resources of a single host machine.

### Benefits

- Virtualization can increase IT agility, flexibility and scalability while creating significant cost savings.
- Greater workload mobility, increased performance and availability of resources, automated operations – they’re all benefits of virtualization that make IT simpler to manage and less costly to own and operate.

## Commands used in Linux

- To find out the name of OS
  `uname` or `uname -a`

- To create a file in Linux
  `touch filename` or `nano filename`

- To check existing file/folders `ls` or `ls -a`
- To create a folder `mkdir foldername`
- To navigate inside the folder `cd foldername`
- To come out of the folder or 1 step back `cd ..`
- To check our current location `pwd`
- `whoami`
- To copy file `cp filename_with_absolute_path destination_with_absolute_path`
- To remove file/folder `rm -rf file/folder_name`
- To cut paste/move the file `mv filename_with_absolute_path foldername_with_absolute_path`
- To rename a file `rename [options] 's/[filename element]/[replacement]/' [filename]`
- To check all processes `top` and `ps aux`
  - a = show processes for all users
  - u = display the process’s user/owner
  - x = also show processes not attached to a terminal
- To use root user `sudo su` or `sudo i`
- To use `|` pipe : [refer](https://opensource.com/article/18/8/introduction-pipes-linux)
- To remove/delete/kill process `sudo kill -9 PID`
- To check file permission `ll`
- change file permission `chmod permission filename`
  - `r` or `w` or `rw` `all` also numbers `400` or `600` for all `700`
- update our ubuntu OS `sudo apt-get update`
- upgrade or ubuntu OS `sudo apt-get upgrade` or `sudo apt-get upgrade -y`
- To create automate tasks with provisioning scripts
  - automate update and upgrade
    - `sudo nano provision.sh`
    - `sudo cat provision.sh`
    - `sudo chmod +x provision.sh`
    - run provision.sh `./provision.sh`
