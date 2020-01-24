
**Cisco Wireless Controller (WLC) with Ansible**

cisco-wlc-commands.yml - an example of a playbook that sends command to the WLC

cisco-wlc-install.yml - an example of a playbook that downloads an image and upgrades the WLC

cisco-wlc-radio.yml - this example captures a specific radio policy from the WLC and outputs to a file

Contacts:

* Jason Mah ( jamah@cisco.com )


**Source Installation**

1) Clone repo

```bash
https://github.com/gve-sw/wlc_ansible.git
```

2) Within the root directory of the application, install pip dependencies (use a virtual environment when possible)

```bash
pip install -r requirements.txt
```

3) Modify the /vars/main.yml files based on your specific parameters.  See example below

```buildoutcfg
creds:
  username: cisco
  password: Cisco123

ftp:
  username: cisco
  password: Cisco123
  ip: 192.168.128.36
  path: /downloads/
  filename: AIR-CT5500-K9-8-2-170-0.aes
  startbootversion: 8.0.152.0
  endbootversion: 8.2.170.0

```

4) Run either playbook file "cisco-wlc-commands.yml" or "cisco-wlc-install.yml" or "cisco-wlc-radio.yml"

```bash
ansible-playbook cisco-wlc-commands.yml
ansible-playbook cisco-wlc-install.yml
ansible-playbook cisco-wlc-radio.yml
```



