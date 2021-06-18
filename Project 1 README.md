Automated ELK Stack Deployment
------------------------------

The files in this repository were used to configure the network depicted
below.

![TODO: Update the path with the name of your
diagram](Images/diagram_filename.png)

These files have been tested and used to generate a live ELK deployment
on Azure. They can be used to either recreate the entire deployment
pictured above. Alternatively, select portions of the \_\_\_\_\_ file
may be used to install only certain pieces of it, such as Filebeat.

-   *TODO: Enter the playbook file.*

This document contains the following details: - Description of the
Topologu - Access Policies - ELK Configuration - Beats in Use - Machines
Being Monitored - How to Use the Ansible Build

### Description of the Topology

The main purpose of this network is to expose a load-balanced and
monitored instance of DVWA, the D\*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly AVAILABLE, in
addition to restricting access to the NETWORK. - \_TODO: What aspect of
security do load balancers protect? AVAILABILITY What is the advantage
of a jump box? IT HELPS SEPERATE ACCESS WITHIN A NETWORK BETWEEN
SECURITY ZONES

Integrating an ELK server allows users to easily monitor the vulnerable
VMs for changes to the JUMPBOX and system NETWORK. - *TODO: What does
Filebeat watch for? LOG FILES OR LOCATIONS - *TODO: What does Metricbeat
record? PERFORMANCE METRICS FROM SYSTEMS AND SERVICES

The configuration details of each machine may be found below. *Note: Use
the [Markdown Table
Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove
values from the table*.

  Name       Function   IP Address   Operating System
  ---------- ---------- ------------ ------------------
  Jump Box   Gateway    10.0.0.1     Linux
  TODO                               
  TODO                               
  TODO                               

### Access Policies

The machines on the internal network are not exposed to the public
Internet.

Only the JUMPBOX PROVISIONER machine can accept connections from the
Internet. Access to this machine is only allowed from the following IP
addresses: - \_TODO: Add whitelisted IP addresses: 173.92.85.2, 10.0.0.4

Machines within the network can only be accessed by ENTERING THE JUMPBOX
PROVISIONER AND ACCESSING DESIRED MACHINE. - \_TODO: Which machine did
you allow to access your ELK VM? What was its IP address? WEB-3.
13.82.224.228 10.0.0.8

A summary of the access policies in place can be found in the table
below.

  Name       Publicly Accessible   Allowed IP Addresses
  ---------- --------------------- ----------------------
  Jump Box   Yes/No                10.0.0.1 10.0.0.2
                                   
                                   

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No
configuration was performed manually, which is advantageous because... -
\_TODO: What is the main advantage of automating configuration with
Ansible? IT REDUCES WORKLOAD BY ALLOWING ONE EDIT TO THE PLAYBOOK TO
AFFECT ALL MACHINES IN THE NETWORK.

The playbook implements the following tasks: - *TODO: In 3-5 bullets,
explain the steps of the ELK installation play. E.g., install Docker;
download image; etc.* - DISABLE FIREWALL OR OPEN PORTS - INSTALL JAVA -
INSTALL ELASTICSEARCH - INSTALL KIBANA - INSTALL LOGSTASH

The following screenshot displays the result of running `docker ps`
after successfully configuring the ELK instance.

![TODO: Update the path with the name of your screenshot of docker ps
output](Images/docker_ps_output.png)

### Target Machines & Beats

This ELK server is configured to monitor the following machines: WEB-1,
WEB-2, WEB-3 - \_TODO: List the IP addresses of the machines you are
monitoring 10.0.0.5, 10.0.0.6, 10.0.0.8

We have installed the following Beats on these machines: - \_TODO:
Specify which Beats you successfully installed: FILEBEAT AND METRICBEATS

These Beats allow us to collect the following information from each
machine: - *TODO: In 1-2 sentences, explain what kind of data each beat
collects, and provide 1 example of what you expect to see. E.g.,
`Winlogbeat` collects Windows logs, which we use to track user logon
events, etc.*

### Using the Playbook

In order to use the playbook, you will need to have an Ansible control
node already configured. Assuming you have such a control node
provisioned:

SSH into the control node and follow the steps below: - Copy the PENTEST
PLAYBOOK file to INSTALL-ELK.YML. - Update the PLAYBOOK file to include:
ELK VM AND NEW HOST, INCREASED MEMORY, DOWNLOAD AND LAUNCH ELK
CONTAINER, ENABLE DOCKER SERVICE ON BOOT. - Run the playbook, and
navigate to LOCALHOST/SETUP.PHP to check that the installation worked as
expected.

*TODO: Answer the following questions to fill in the blanks:* - *Which
file is the playbook? Where do you copy it? PENTEST.YML.
INSTALL-ELK.YML. - *Which file do you update to make Ansible run the
playbook on a specific machine? PENTEST.YML How do I specify which
machine to install the ELK server on versus which to install Filebeat
on? HOSTS SECTION OF .YML FILE - \_Which URL do you navigate to in order
to check that the ELK server is running? HTTP://SETUP.PHP

*As a **Bonus**, provide the specific commands the user will need to run
to download the playbook, update the files, etc.*
