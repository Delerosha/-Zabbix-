Задание 1
<img width="2495" height="1069" alt="Zabbix-web" src="https://github.com/user-attachments/assets/765f8514-1340-4adf-9b43-72013527e4d1" />
## Задание 1

```bash
sudo apt update
sudo apt install postgresql postgresql-contrib
sudo apt install dpkg 
wget https://repo.zabbix.com/zabbix/6.0/ubuntu/pool/main/z/zabbix-release/zabbix-release_latest_6.0+ubuntu24.04_all.deb
dpkg -i zabbix-release_latest_6.0+ubuntu24.04_all.deb
sudo apt update
sudo apt install zabbix-server-pgsql zabbix-frontend-php php8.1-pgsql zabbix-apache-conf zabbix-sql-scripts
sudo -u postgres createuser --pwprompt zabbix
sudo -u postgres createdb -O zabbix zabbix
zcat /usr/share/zabbix-sql-scripts/postgresql/server.sql.gz | sudo -u zabbix psql zabbix 
systemctl restart zabbix-server apache2
systemctl enable zabbix-server apache2


Задание 2
<img width="2487" height="790" alt="Zabbix 2 2 dz" src="https://github.com/user-attachments/assets/b82f97bd-f726-4e5d-bebd-c4e581572c58" />
<img width="2479" height="1222" alt="Zabbix 2 3 dz" src="https://github.com/user-attachments/assets/09d24f20-ccc0-40af-bdeb-9d91126fe1bb" />
<img width="1215" height="623" alt="Zabbix 2 4" src="https://github.com/user-attachments/assets/62814ba6-4136-47af-82b7-6c4a00475744" />

## Задание 2

```bash
wget https://repo.zabbix.com/zabbix/6.0/ubuntu/pool/main/z/zabbix-release/zabbix-release_latest_6.0+ubuntu24.04_all.deb
dpkg -i zabbix-release_latest_6.0+ubuntu24.04_all.deb
sudo apt install dpkg
sudo apt update
sudo apt install zabbix-agent
systemctl restart zabbix-agent
systemctl enable zabbix-agent
