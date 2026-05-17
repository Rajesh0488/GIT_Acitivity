**Interactive Log Script**

# 1️ Navigate to Scripts Directory

cd /home/ec2-user/webapp/scripts/

<img width="940" height="57" alt="image" src="https://github.com/user-attachments/assets/48595bb4-287d-4dc1-9899-04d48ac09a63" />

# 2️ Create Script Using Vim

vim log_user.sh

<img width="909" height="69" alt="image" src="https://github.com/user-attachments/assets/6fc29ae6-2dc4-4c4a-83dc-3aa32b522a5f" />

#!/bin/bash
read -p "Enter your name: " username

cat /home/ec2-user/webapp/config/app.conf

echo "Login: $username Date: $(date)" >> /home/ec2-user/webapp/logs/app.log

cat /home/ec2-user/webapp/logs/app.log

Save and exit:
Esc → :wq

<img width="940" height="720" alt="image" src="https://github.com/user-attachments/assets/e8b821c3-4705-4463-9d88-e3dd88ea992f" />


# 3️ Give Execute Permission

chmod +x log_user.sh

<img width="940" height="270" alt="image" src="https://github.com/user-attachments/assets/9fbb9d39-644e-4103-b01e-7ae35df94422" />

# 4️ Run Script Multiple Times

Run the script at least 3 times:

./log_user.sh

<img width="795" height="285" alt="image" src="https://github.com/user-attachments/assets/3b767ef0-f4f6-4292-8c7b-37fcf1aad22f" />

# 5️ Verify Log File

cat /home/ec2-user/webapp/logs/app.log

<img width="940" height="101" alt="image" src="https://github.com/user-attachments/assets/1c91ef5d-18d0-4aec-be67-cf40ec027409" />
