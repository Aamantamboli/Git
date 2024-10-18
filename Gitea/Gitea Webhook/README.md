# Gitea Webhooks

### Step 1: Create one Instance for Jenkins 

![image](https://github.com/user-attachments/assets/48a1893d-ff85-4117-9642-e6639da8d934)

### Step 2: Create another Instance for Gitea 

![image](https://github.com/user-attachments/assets/a61c233b-7157-4af3-a454-3c3ac964b0bd)

### Step 3: Install Jenkins in Jenkins server [(you can refer here for installation)](https://github.com/Aamantamboli/Jenkins/tree/main/Jenkins%20Installation)
### Step 4: Install Gitea in Gitea server [(you can refer for installation)](https://github.com/Aamantamboli/Install-and-Configure-Gitea.git)
### Step 5: Connect Jenkins server with it's public IP and 8080 port and Connect Gitea server with it's public IP with 3000 port
### Step 6: Create a Repository in Gitea 

![image](https://github.com/user-attachments/assets/ae33329c-ef0b-4f7f-a78e-ac4040069fb1)

### Step 7: Create a new File in Repository 

![image](https://github.com/user-attachments/assets/6d7b7016-e49a-45c4-92fc-83df9f007bb0)

### Step 8: Now in Jenkins Go to Manage Jenkins > Plugins and Install plugins
1.Gitea plugin <br>
2.Git

### Step 9: Create New Item 
Enter an item name <br>
Select Pipeline <br>
Click on OK

![image](https://github.com/user-attachments/assets/13096741-6246-4fc6-9824-fb1b36b22b93)

### Step 10: Click on checkbox Poll SCM 

![image](https://github.com/user-attachments/assets/f9430f27-247f-48a9-84f1-fd879dc824d2)

### Step 11: Select Pipeline script from SCM and paste URL of your repository

![image](https://github.com/user-attachments/assets/5646dbb1-74bf-4939-9444-e2015bf243f8)

### Step 12: Click on Add in credentials fill your username and password of gitea repository 

![image](https://github.com/user-attachments/assets/372e25f2-5985-4ea8-9f7b-2c592d46c87a)

### Step 13: Make changes in Branches to build and save it

![image](https://github.com/user-attachments/assets/f47b1e89-874e-4827-b62d-16f6a8fe801d)

### Step 14: Now Go to Gitea Server > Setting > Webhooks > Gitea

![image](https://github.com/user-attachments/assets/a8cc7167-6925-4d2a-a4de-309d2d2e8510)

### Step 15: Now paste your jenkins URL http:<jenkins_server>/gitea-webhook/post and Add webhook

![image](https://github.com/user-attachments/assets/7a6da9cf-24eb-477e-b0a2-119dbc3f7434)

### Step 16: Now for testing go to your file and make some changes and commit 

![image](https://github.com/user-attachments/assets/c70eeddb-cc74-4ec0-9fa7-e2a43787e4b1)

### Step 17: Now go to Jenkins server and check your pipeline is running

![image](https://github.com/user-attachments/assets/61d83532-af2f-4bf6-b665-ee3e0e816f44)
