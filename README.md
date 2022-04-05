# CyberSec-Bootcamp-Project-1
Project #1 for my cybersecurity bootcamp, containing Linux scripts and Ansible scripts.

## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.

![Azure Research Group](https://github.com/pilot0195/CyberSec-Bootcamp-Project-1/blob/main/diagrams/Azure_Research_Group.png)

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the _____ file may be used to install only certain pieces of it, such as Filebeat.

  - _https://github.com/pilot0195/CyberSec-Bootcamp-Project-1/blob/main/ansible/filebeat-playbook.yml__
  - _https://github.com/pilot0195/CyberSec-Bootcamp-Project-1/blob/main/ansible/metricbeat-playbook.yml__

This document contains the following details:
- Description of the Topologu
- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the D*mn Vulnerable Web Application.

Load balancing ensures that the application will be highly responsive, in addition to restricting access to the network.
- What aspect of security do load balancers protect? What is the advantage of a jump box?_
- The load balancer analyzes incoming traffic and directs it between available servers, protecting against DDoS attacks because the traffic is evenly distributed. A jump box allows finer control over who is able to access a virtual network, because the other virtual machines maintain private IPs that an individual would need in order to access them.

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the logs and system traffic.
- What does Filebeat watch for?
- Filebeat generates and organizes log files, and it watches for changes in files and when these changes occur.
- What does Metricbeat record?
- Metricbeat records data from the OS and the services running on the server. The statistics and metrics can be visualized by using Elasticsearch or Logstash.

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

|   Name   |  Function  | IP Address | Operating System |
|:--------:|:----------:|:----------:|:----------------:|
| Jump Box | Gateway    |  10.0.0.4  |       Linux      |
| DVWA 1   | Web Server |  10.0.0.5  |       Linux      |
| DVWA 2   | Web Server |  10.0.0.6  |       Linux      |
| ELK      | Monitoring |  10.1.0.5  |       Linux      |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the Jump-Box-Provisioner machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- 104.63.15.193 (my public IP)

Machines within the network can only be accessed by the Jump-Box-Provisioner virtual machine.
- Which machine did you allow to access your ELK VM? What was its IP address? Jump-Box-Provisioner (23.99.200.41)

A summary of the access policies in place can be found in the table below.

|   Name   | Publicly Accessible | Allowed IP Addresses |
|:--------:|:-------------------:|:--------------------:|
| Jump Box |         Yes         |     104.63.15.193    |
| ELK      |          No         |       10.0.0.4       |
| DVWA 1   |          No         |       10.0.0.4       |
| DVWA 2   |          No         |       10.0.0.4       |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- Automating configuration with Ansible is advantageous because it streamlines the process for building containers, allowing them to be easily built or torn apart.

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ...
- ...

The following screenshot displays the result of running `docker ps` after successfully configuring the ELK instance.

![TODO: Update the path with the name of your screenshot of docker ps output](Images/docker_ps_output.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_

We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the _____ file to _____.
- Update the _____ file to include...
- Run the playbook, and navigate to ____ to check that the installation worked as expected.

_TODO: Answer the following questions to fill in the blanks:_
- _Which file is the playbook? Where do you copy it?_
- _Which file do you update to make Ansible run the playbook on a specific machine? How do I specify which machine to install the ELK server on versus which to install Filebeat on?_
- _Which URL do you navigate to in order to check that the ELK server is running?

_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._
