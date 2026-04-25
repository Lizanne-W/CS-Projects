Installing, configuring and operating T-Pot Honeypot <br/>

[T-Pot](https://github.com/telekom-security/tpotce) features a suite of honeypots deployed within Docker containers and uses an ELK Stack to process and visualize the resulting telemetry. <br/>
<br/>
Here I will show the step by step process on how to install T-Pot on Microsoft Azure. (For safety reasons, please do not install honeypots on your home/personal computer) <br/>
If you are a student or a new Azure user, you get $200 free credits for 1 month. <br/>
T‑Pot needs 8–16 GB of system memory and at least 128 GB of unused disk space to install and operate correctly. <br/>
Create VM
<img width="1512" height="405" alt="image" src="https://github.com/user-attachments/assets/369c1669-84f7-473a-b075-260446bcba54" />

Create a new resource group if you haven't already created one. <br/>
Name the Virtual Machine <br/>
Select the Standard security type and the OS you're comfortable with; <br/>
<img width="832" height="121" alt="image" src="https://github.com/user-attachments/assets/cd531dad-72a7-4940-82b4-c9b6be4b78af" /> <br/>
Fill in a Username and password or generate a SSH public key <br/>
Review + Create <br/>

Once the VM is created, copy the ip address of the VM <br/>
Don't forget to edit the inbound Security rules in the NSG to allow port 22 for ssh.
<img width="2245" height="543" alt="image" src="https://github.com/user-attachments/assets/4b6a1b94-35ca-437e-8a8b-83c0165282b8" /> <br/>
Start the VM in the Azure GUI <br/>
Once the VM completes the start up, you will be able to ssh in to the VM via the ip address using any ssh client. <br/>
Click [Here](https://github.com/telekom-security/tpotce?tab=readme-ov-file#tldr) for the installation steps from the offical site or see the steps below: <br/>.
Once you ssh in to the VM; <br/>
sudo apt update && sudo apt upgrade -y <br/>
env bash -c "$(curl -sL https://github.com/telekom-security/tpotce/raw/master/install.sh)" <br/>
Choose Y <br/>
Choose "h" for Hive TPot standard <br/>
user: (create a username)<br/>
confirm with 'y' <br/>
pass: (create a password) <br/>
sudo reboot <br/>





