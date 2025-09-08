# Quick Steps

1) Unzip this project in WSL:
```bash
sudo apt update && sudo apt install -y unzip
unzip cmpe272-ansible-webserver-with-your-ips.zip -d ~/cmpe272-ansible-webserver
cd ~/cmpe272-ansible-webserver
```

2) Test connectivity:
```bash
ansible -i inventory.ini webservers -m ping
```

3) Deploy:
```bash
ansible-playbook -i inventory.ini site.yml --tags deploy
```

4) Check in browser:
- http://3.20.232.179:8080  → SJSU-1
- http://3.144.134.79:8080 → SJSU-2

5) Undeploy:
```bash
ansible-playbook -i inventory.ini site.yml --tags undeploy
```
