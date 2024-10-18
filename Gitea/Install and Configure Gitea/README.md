# Install-and-Configure-Gitea
### Step 1: Create Instance 
<strong>(MUST HAVE 3000 PORT IN SECURITY GROUP)</strong>

![image](https://github.com/user-attachments/assets/dd1a575b-264b-4073-9c3f-bb8793aa1a3a)

### Step 2: The command sudo -i && sudo apt update allows you to switch to the root user and update the package list on a Debian-based system.
```
sudo -i
sudo apt update
```
### Step 3: The command installs PostgreSQL and its additional contributed modules, automatically confirming any prompts.
```
sudo apt install postgresql postgresql-contrib -y 
```
### Step 4: The command sets PostgreSQL to start automatically at boot time on a system using systemd.
```
sudo systemctl enable postgresql.service
```
### Step 5: The command opens a new shell as the PostgreSQL user, allowing you to execute commands with PostgreSQL privileges.
```
sudo -i -u postgres
```
### Step 6: The command launches the PostgreSQL interactive terminal, allowing you to execute SQL queries and manage your PostgreSQL databases.
```
psql
```
### Step 7: The command creates a new PostgreSQL role named with login privileges and sets its password 
```
CREATE ROLE gitea WITH LOGIN PASSWORD 'gitea';
```
### Step 8: The command creates a new PostgreSQL database named owned by the role, using the UTF-8 encoding and specified locale settings.
```
CREATE DATABASE gitea WITH OWNER gitea TEMPLATE template0 ENCODING UTF8 LC_COLLATE 'en_US.UTF-8' LC_CTYPE 'en_US.UTF-8';
```
### Step 9: The command terminates the current shell session or closes the PostgreSQL interactive terminal.
```
\q
```
### Step 10: The command opens the PostgreSQL client authentication configuration file in the Vim text editor with superuser privileges for editing.
```
sudo vim /etc/postgresql/16/main/pg_hba.conf
```
<strong>(host  all  all 0.0.0.0/0 scram-sha-256  edit like this line)</strong><br>

![image](https://github.com/user-attachments/assets/c2e1e290-5b51-416d-a701-3848926f7438)
### Step 11: The command opens the main PostgreSQL configuration file in the Vim text editor with superuser privileges for editing.
```
sudo vim /etc/postgresql/16/main/postgresql.conf
```
**(listen_addresses = '*' edit this line)**<br>

![image](https://github.com/user-attachments/assets/cc4bda94-9952-41eb-9d60-ffea995f47da)

### Step 12: The command updates the package list, upgrades installed packages, and installs Git, automatically confirming any prompts.
```
sudo apt update && sudo apt upgrade -y && sudo apt install git -y
```
### Step 13: The commands download the Gitea binary and make it executable.
```
wget -O gitea https://dl.gitea.com/gitea/1.21/gitea-1.21-linux-amd64
chmod +x gitea
```
### Step 14: The command creates a system user named "git" with a specific home directory and no login password, for Git version control purposes.
```
sudo adduser --system --shell /bin/bash --gecos 'Git Version Control' --group --disabled-password --home /home/git git
```
### Step 15: The commands create necessary directories for Gitea, set ownership and permissions to ensure the "git" user has access, and configure the Gitea configuration directory with appropriate permissions.
```
sudo mkdir -p /var/lib/gitea/custom
sudo mkdir -p /var/lib/gitea/data
sudo mkdir -p /var/lib/gitea/log
sudo chown -R git:git /var/lib/gitea/
sudo chmod -R 750 /var/lib/gitea/
sudo mkdir /etc/gitea
sudo chown root:git /etc/gitea
sudo chmod 770 /etc/gitea
```
### Step 16: The command sets the environment variable GITEA_WORK_DIR to specify the working directory for Gitea.
```
export GITEA_WORK_DIR=/var/lib/gitea/
```
### Step 17: The command copies the Gitea binary to the /usr/local/bin directory, making it accessible system-wide.
```
sudo cp gitea /usr/local/bin/gitea
```
### Step 18: The command opens the Gitea service configuration file in the Vim text editor with superuser privileges for editing.
```
sudo vim /etc/systemd/system/gitea.service
```
**(Copy the following content into the service file)<br>**
```
[Unit]
Description=Gitea (Git with a cup of tea)
After=syslog.target
After=network.target
[Service]
RestartSec=2s
Type=simple
User=git
Group=git
WorkingDirectory=/var/lib/gitea/
ExecStart=/usr/local/bin/gitea web -c /etc/gitea/app.ini
Restart=always
Environment=USER=git HOME=/home/git GITEA_WORK_DIR=/var/lib/gitea

[Install]
WantedBy=multi-user.target
```
### Step 19: The commands enable the Gitea service to start on boot and immediately start the service, respectively.
```
systemctl enable gitea.service
systemctl start gitea.service
```
### Step 20: Paste the public IP of Instance with 3000 port

![image](https://github.com/user-attachments/assets/e5767fd1-4a47-4295-84d2-84ab791f841c)

### Step 21: Create a new file in repository

![image](https://github.com/user-attachments/assets/34070127-97b7-49ff-9542-90cb7303bc60)

```
git clone http://65.0.76.229:3000/Aamantamboli/new.git
cd new/
```
### Step 22: Now pull it from repository

![image](https://github.com/user-attachments/assets/87f9b50f-8a45-44e1-9449-fa1b075fc8b0)

**Successfully configure Gitea and pull repository**
