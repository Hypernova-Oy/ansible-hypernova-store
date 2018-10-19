# Ansible
Nginx / PHP-FPM 7.2, Magento2 or Wordpress, Redis server cache, MariaDB, Fail2ban, Postfix relay to Mailgun, Firewall, Letsencrypt, and Linux malware detect. Ubuntu 18.04

## Add new user
This command will add provided username with the same key and password into all hosts

`ansible-playbook server.yml --extra-vars="new_user_name=kelvin" --tags addusers`

You may find a report and keys into ~/ansible_users_keys directory.

To have more secure a four randomly generated charset will add to login `kelvin` and new login will like this `kelvinbfqp`. Password has 20 charsets. Keys will have names `kelvinbfqp_id_rsa kelvinbfqp_id_rsa.pub`

The example report:

    The new user has been successfully created
    Login: kelvinbfqp
    Password: hDRXFMxvKz38ribod0ro
    Key: ~/ansible_users_keys/kelvinbfqp_id_rsa
    Date: 2018-10-18
    =========================================
    SSH:
    ssh -i ~/ansible_users_keys/kelvinbfqp_id_rsa kelvinbfqp@192.168.182.128
    ssh -i ~/ansible_users_keys/kelvinbfqp_id_rsa kelvinbfqp@192.168.182.129
