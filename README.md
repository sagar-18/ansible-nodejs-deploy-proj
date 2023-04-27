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
and add hosts ip address - e.g. 164.92.249.174

<img width="691" alt="Screenshot 2023-04-27 at 11 55 08 AM" src="https://user-images.githubusercontent.com/36581523/234777380-39b83dcd-d4a9-44a5-b922-6bba9425c82b.png">

Step 8: Create the playbook file

<img width="968" alt="Screenshot 2023-04-27 at 4 24 58 PM" src="https://user-images.githubusercontent.com/36581523/234842028-41a8a73a-0b44-4f4a-b873-ad48808fdbac.png">

Step 9: Run this playbook file now 
Command: sudo ansible-playbook -i /etc/ansible/inventory deploy_task_manager.yml 

<img width="1512" alt="Screenshot 2023-04-27 at 4 19 29 PM" src="https://user-images.githubusercontent.com/36581523/234840857-151d1e79-1316-47a3-aa00-77b3180770f9.png">

Step 10: 

<img width="573" alt="Screenshot 2023-04-27 at 4 23 24 PM" src="https://user-images.githubusercontent.com/36581523/234841720-353e001f-dfa6-40a6-9159-5ba8254215ff.png">


APP IS LIVE ON HOST NODE:

<img width="869" alt="Screenshot 2023-04-27 at 4 19 53 PM" src="https://user-images.githubusercontent.com/36581523/234840930-d25c1a3c-974c-4174-a946-903f90d196f1.png">
