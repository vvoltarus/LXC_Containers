To check all containers we can type:
<code>lxc-ls --fancy</code>

We can reconfigure the container to autostart by added a line to the container's configuration.
<code>echo "lxc.start.auto = 1" >>/var/lib/lxc/mycontainer/config</code>

Now reboot the machine:
<code>reboot</code>

After allowing the host some time to reboot and signing back into the host's shell, we see that the container is running and has the autostart property set to 1.

![alt text](https://github.com/vvoltarus/LXC_Containers/blob/main/pics/autostart_1.png)

If we want several of the containers we create to have autostart, then we might prefer to create a new configuration file to use with <code>lxc-create</code>

<code>cp /etc/lxc/default.conf /etc/lxc/autostart.conf
echo "lxc.start.auto = 1" >>/etc/lxc/autostart.conf
lxc-create --name containera --config /etc/lxc/autostart.conf --template download -- --dist alpine --release 3.19 --arch amd64
</code>
