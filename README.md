# ansible-nodejs-deploy-proj
Setting up Nodejs Application using ansible

OS: Ubuntu 22 (Control Node)

Step 1: Update OS

sudo apt update 

Step 2: Install Ansible

sudo apt install ansible

Step 3: Check if it is installed

sudo ansible --version

<img width="1328" alt="Screenshot 2023-04-27 at 11 35 41 AM" src="https://user-images.githubusercontent.com/36581523/234773662-aaeb9645-0c8a-4f7e-aa7e-54ff425c9ed8.png">

Step 4: Generate an SSH key pair on the control node

ssh-keygen

Step 5: Copy the public key from control to the host server

ssh-copy-id usernameofhost@ipaddressofhostserver

Step 6: Test the SSH connection

You can test the SSH connection from the control node to the host server using the following command:

ssh hostuser@host_ip_address

<img width="854" alt="Screenshot 2023-04-27 at 11 46 43 AM" src="https://user-images.githubusercontent.com/36581523/234775766-cd9e9ef9-0988-43e8-9814-15096b26793e.png">

Step 7: Create the inventory file

sudo vim /etc/ansible/hosts
and add hosts ip address - e.g. 65.0.105.243

<img width="691" alt="Screenshot 2023-04-27 at 11 55 08 AM" src="https://user-images.githubusercontent.com/36581523/234777380-39b83dcd-d4a9-44a5-b922-6bba9425c82b.png">

Step 8: Create the playbook file






