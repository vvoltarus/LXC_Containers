If we want to make a predictable IP adress we need to make some changes on LXC config file.

To enable DHCP reservations, we uncomment the <code>LXC_DHCP_CONFILE</code> line in <code>/etc/default/lxc-net </code>.

<code># sed -i 's|^#LXC_DHCP_CONFILE=.*$|LXC_DHCP_CONFILE=/etc/lxc/dnsmasq.conf|' /etc/default/lxc-net</code>

Add the DHCP reservation.

<code># echo "dhcp-host=server_test,10.0.3.200" >>/etc/lxc/dnsmasq.conf </code>

Restart the lxc-net service so the DHCP reservation is enabled.

<code># service lxc-net restart </code>

Restart the container.

<code> # lxc-stop --name server_test </code>
<code># lxc-start --name server_test</code>
