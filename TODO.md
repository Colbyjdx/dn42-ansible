~~- Separate everything out into roles~~
- Role / support for non-routers
- Webserver role (with nginx, bird-lg, Grafana, certbot)
- Monitoring (Grafana / Telegraf / etc)
- Iptables (make actual rules)
~~- Region & country neighbourhoods~~
- iperf3 (plus systemd service)
- Support dyanmic IPs (refresh Wireguard DNS every now and then)
- DNS servers (bind9?)
- Automatic OSPF cost calculation (ping other nodes every X minutes to calculate)
~~- DN42 pingfinder~~
- (Ansible) Consolidate recurring handlers into a global thing ?
- RTR server? https://dn42.dev/howto/Bird2 https://dn42.eu/howto/ROA-slash-RPKI
