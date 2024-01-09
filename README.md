# Overview
This is my Ansible repository for managing my [dn42](https://dn42.dev/) network [COLBY-NET / AS4242422558](https://dn42.derix.dev/). This project is my first time using/learning Ansible, so it's probably not following all the best practices, but it works for me! Maybe it'll be useful to someone else.

Inspired by jlu5's [dn42-ansible](https://github.com/jlu5/ansible-dn42) repository.

For another dn42-related Ansible project, see my [ansible-ping-matrix](https://github.com/Colbyjdx/ansible-ping-matrix) repository.

# Adding a new host
* Generate a Wireguard keypair using `{ WGK=$(wg genkey); echo -e "Private:  $WGK\nPublic:   $(echo $WGK | wg pubkey)"; unset WGK; }`
* Add them to `hosts.yml`, filling out all the same fields as the other hosts
* Add them to either the `dn42_full` or `dn42_lite` group, depending on the virtualisation type
* Add their IPs to all zonefiles
* Add their pingfinder UUID & wg private key in the secrets file
