###Linux Containers - LXC###

**Step 1 - Installation**
First of all lets install the lxc.

<code>sudo apt-get install lxc </code>

**Step 2 - Create Privileged Containers**
Privileged containers are containers that are created by root and run as root.
Remember all commands we do with SUDO.
The list of all images for containers : https://images.linuxcontainers.org/

<code>lxc-create --name server_test --template download -- --dist centos --release 8-Stream --arch amd64 </code>

After creating the container, we need to start it:
<code>lxc-start --name server_test </code>

Type <code>lxc-info --name server_test</code> to see if the container running.

<img>create_container</img>

Start a container shell:
<code>lxc-attach --name server_test	</code>

Update the package index, upgrade installed packages, and install more packages you would like available:
<code>
yum update
yum upgrade
yum install vim python3 -y
</code>

Install autocomplete TAB --Not required.
<code> yum install bash-completion</code>

Exit and login again and check autocomplete with TAB.

To stop and destroy our container type:

<code> lxc-stop --name server_test
       lxc-destroy --name server_test</code>
	   
