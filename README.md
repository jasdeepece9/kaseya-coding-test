Prerequisites:-
==============
- First you need to create a Jenkins and Windows EC2 machines with Windows 2012 R2 or later in AWS Account. You can use t2.micro EC2 instance type which is free(750hrs of free usage per month)

- Then login to Jenkins EC2 machine and install Jenkins on it.

- Install ansible on Jenkins EC2 machine (Use Yum to install it as i am using Linux EC2 for Jenkins Server).

- Next step is to install the Ansible Plugin on Jenkins by going to Manage Plugins in Jenkins UI.

- Next configure the Ansible installation path under Global Tool Configuration.

- Next install GIT on your Jenkins EC2 machine.

- Next is to create an ansible playbook named windows.yml which should update the Windows VM.

- Finally, create a new Pipeline Job which will trigger this ansible playbook that we created in pervious step.
