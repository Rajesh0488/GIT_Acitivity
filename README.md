User Management & File Permission Control

Create Linux users and control access to a script using:

* Groups
* File ownership
* Permissions

Two users will have **write access**, and two users will have **read-only access** to the script.

# 1️ Create Group

sudo groupadd writers

<img width="940" height="29" alt="image" src="https://github.com/user-attachments/assets/40cd7f46-acce-4f71-afaf-48923b7c31c2" />

# 2️ Create Users

sudo useradd -m devuser1

sudo useradd -m devuser2

sudo useradd -m devuser3

sudo useradd -m devuser4

<img width="940" height="112" alt="image" src="https://github.com/user-attachments/assets/253a654c-537b-43e0-8802-0875e5573199" />

<img width="863" height="197" alt="image" src="https://github.com/user-attachments/assets/a5686076-53da-4030-a33b-9d209f3f00fc" />

# 3️ Add Users to Writers Group

sudo usermod -aG writers devuser1

sudo usermod -aG writers devuser2

<img width="940" height="56" alt="image" src="https://github.com/user-attachments/assets/395d9bc1-aee7-4038-a38f-a308a04b5672" />

<img width="744" height="188" alt="image" src="https://github.com/user-attachments/assets/f0cada3b-b70b-4951-b420-2d95063b6d94" />

# 4️ Change Group Ownership of Script

sudo chown root:writers /home/ec2-user/webapp/scripts/log_user.sh

<img width="940" height="71" alt="image" src="https://github.com/user-attachments/assets/6dd9c825-a1f1-49c1-b44a-28b7ef8008f6" />

# 5️ Set File Permissions

sudo chmod 664 /home/ec2-user/webapp/scripts/log_user.sh

# Verify Permissions

ls -l /home/ec2-user/webapp/scripts/log_user.sh

<img width="940" height="78" alt="image" src="https://github.com/user-attachments/assets/7fff13e3-7c14-4a4b-b7b9-746cc00cc388" />

# Test Write Access (Allowed Users)

su - devuser1

echo "test" >> /home/ec2-user/webapp/scripts/log_user.sh

<img width="940" height="562" alt="image" src="https://github.com/user-attachments/assets/67cbe9c5-012d-4753-a9ca-5457d92e8841" />

<img width="940" height="261" alt="image" src="https://github.com/user-attachments/assets/1abca8f3-879f-4963-aa1a-a5724e45e734" />

# Test Read-Only Access

su - devuser3

cat /home/ec2-user/webapp/scripts/log_user.sh

echo "test" >> /home/ec2-user/webapp/scripts/log_user.sh

<img width="940" height="548" alt="image" src="https://github.com/user-attachments/assets/b2f67837-4896-4453-bdac-e6acc9cb4a90" />


