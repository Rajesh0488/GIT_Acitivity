Create a complete project directory structure, apply correct permissions, and set ownership. This structure will be used in further automation scripts.

# 1️ Create Directory Structure

Use a single command to create all required directories:

sudo mkdir -p /home/ec2-user/webapp/{scripts,logs,config}

<img width="940" height="58" alt="image" src="https://github.com/user-attachments/assets/2fd19972-f9a8-4654-b477-26b857e12f69" />

# 2️ Create Configuration File

cat > /home/ec2-user/webapp/config/app.conf
Add the following content:

APP_NAME=WebApp
PORT=8080

Save the file using:
**Ctrl + D**

<img width="940" height="114" alt="image" src="https://github.com/user-attachments/assets/e42f584b-7a03-41b2-8bdc-647a397b4dd2" />

# 3️ Create Log File

touch /home/ec2-user/webapp/logs/app.log

ls -l /home/ec2-user/webapp/logs/app.log

<img width="940" height="84" alt="image" src="https://github.com/user-attachments/assets/7ef8521b-7b9e-4aba-acb4-220e8c7eceb4" />

<img width="940" height="74" alt="image" src="https://github.com/user-attachments/assets/4b68bacf-275e-401b-a90f-2a713b6a5454" />

# 4️ Set Permissions

chmod 755 /home/ec2-user/webapp/scripts
chmod 644 /home/ec2-user/webapp/config/app.conf

<img width="940" height="86" alt="image" src="https://github.com/user-attachments/assets/87846a9e-5375-45c8-981a-9e9d85bd5394" />

# 5️ Change Ownership

sudo chown -R root:root /home/ec2-user/webapp/

# 6️ Verify Structure

ls -lR /home/ec2-user/webapp/

<img width="940" height="531" alt="image" src="https://github.com/user-attachments/assets/63d34c31-faaf-4748-94f7-4b6b50734d1c" />
