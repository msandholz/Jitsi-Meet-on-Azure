Create VM on Azsure



1. SSH to VM: 'markus_sandholz@Azure:~$ ssh azureuser@20.71.207.224'
2. Set Timezone: 'sudo timedatectl set-timezone Europe/Berlin'

NGINX installation
1. Update LINUX: 'sudo apt update'
2. Install NGINX: 'sudo install nginx'
3. Enable NGNIX: 'sudo systemctl enable nginx'

Jitsi Meet installation
1. Getting root access: 'sudo bash'
2. Edit FQDN: 'nano /etc/hosts' --> '127.0.0.1 localhost jitsi.sandholz.de' ???
3. Add Jitsi package repository: 
  a) 'echo 'deb https://download.jitsi.org stable/' >> /etc/apt/sources.list.d/jitsi-stable.list'
  b) 'wget -qO -  https://download.jitsi.org/jitsi-key.gpg.key | sudo apt-key add -'
4. Enable https apt repositories then we can install Jitsi Meet:
  a) 'apt-get install apt-transport-https'
  b) 'apt update'
  c) 'apt-get -y install jitsi-meet'
5. Hostname of video-bridge: 'jitsi-videobridge'
6. Generate Certificate: '/usr/share/jitsi-meet/scripts/install-letsencrypt-cert.sh' 
