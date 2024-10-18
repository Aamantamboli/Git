# GitHub Webhook
## GitHub Webhook for Public Repository
### Step 1: Create one Instance for Jenkins

![image](https://github.com/user-attachments/assets/473b34fc-e9a0-4476-a486-49fb77486c0f)

### Step 2: Install Jenkins in Jenkins server [(you can refer for installation)](https://github.com/Aamantamboli/Jenkin-Installation.git)
### Step 3: Connect Jenkins server with it's public IP and 8080 port 
### Step 4: Create new item
Enter an item name
Select Pipeline
Click on OK

![Screenshot 2024-10-16 113743](https://github.com/user-attachments/assets/7b8db88a-04da-42d4-b570-6440dd079091)

### Step 5: Click on checkbox GitHub project and provide URL of repository also click on checkbox GitHub hook trigger for GITScm polling for trigerring

![Screenshot 2024-10-16 113810](https://github.com/user-attachments/assets/d25f6521-211c-42c9-ae82-5a37d40a6d3e)

### Step 6: Select Pipeline script from SCM and paste URL of your repository

![Screenshot 2024-10-16 113838](https://github.com/user-attachments/assets/aa9cce73-682e-4e2f-bc06-0484db03a26a)

### Step 7: Make changes in Branches to build and save it

![Screenshot 2024-10-16 113856](https://github.com/user-attachments/assets/1df119e7-049f-4c70-87bb-7948a0249c40)

### Go to GitHub, create new file and save it with namaing as Jenkinsfile 

![Screenshot 2024-10-16 113729](https://github.com/user-attachments/assets/291b7507-2346-434f-8325-e31c04ee11ef)

### Step 8: Click on setting go to webhook and add webhook

![Screenshot 2024-10-16 113951](https://github.com/user-attachments/assets/9a19d54d-de27-4c23-9fc0-3910c916a445)

### Step 9: In payload URL give url of jenkins server and content type application/json as shown below and save it 

![Screenshot 2024-10-16 114139](https://github.com/user-attachments/assets/6f893a2e-5362-44e5-b4db-a18b3e1db345)

### Step 10: Go to recent deliveries and must check is it integrated or not 

![Screenshot 2024-10-16 114349](https://github.com/user-attachments/assets/e8bc15c3-6a5f-42a9-8fff-ebbc56be7c2e)

### Step 11: Go to file and make some changes 

![Screenshot 2024-10-16 114421](https://github.com/user-attachments/assets/c007c3e8-f2a7-425c-914c-c909d88ee320)

## Step 12: As soon you make changes pipeline will be triggered and start running automatically 

![Screenshot 2024-10-16 114435](https://github.com/user-attachments/assets/b4d01aa5-a564-43bc-8221-164b16f6aa5d)


## GitHub Webhook for Private Repository by ssh key 
## GitHub Webhook for Private Repository by token 

