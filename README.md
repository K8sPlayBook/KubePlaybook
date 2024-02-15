# KubePlaybook
Ansible playbook repository for Kubernetes (K8s)

# Ansible Playbook Generation with GPT-4

This repository contains Ansible playbooks,  a dataset featuring 130 Ansible playbooks accompanied by natural language(NL) prompts designed for code generation. NL prompts, serving as queries or descriptions in natural language, instruct LLMs to generate task-specific code. The playbooks are designed to automate deployment tasks, ensuring reliability and efficiency in real-world production environments. Ansible playbooks are classified into three primary categories, each comprising pairs of playbooks and corresponding NL prompts. These categories encompass essential K8s commands, Ansible Galaxy and GitHub integration, and playbook for mitigating chaos-engineered operational faults.

## Evaluation Process

Testing occurred on a t2.2xlarge EC2 instance with Ubuntu, where we installed Robot-shop and QoTD. We validated both syntactic correctness and functional soundness during this phase, focusing on the effectiveness of automated deployment.

## Installation and Usage

1. Clone this repository:
   

         git clone https://github.com/K8sPlayBook/KubePlaybook.git


2. Install Ansible and required dependencies:

   
         pip install ansible

         snap install microk8s --classic

         microk8s.kubectl version


4. Create a host file for the microservices:
   
      Example host file (hosts.ini):

            [local]

            localhost ansible_connection=local

            [k8s]

            ip-XXX-XX-X-XXX ansible_connection=local


4. Run the Ansible playbooks:
   
         ansible-playbook -i hosts.ini playbook.yml

## Acknowledgments

We would like to thank and acknowledge the developers of Robot-shop and QoTD for their valuable contributions to the testing environment.


For more detailed instructions, refer to the paper[yet to publish).
