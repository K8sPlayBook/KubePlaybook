# KubePlaybook

![example event parameter](https://github.com/github/docs/actions/workflows/main.yml/badge.svg?event=push)


Ansible playbook repository for Kubernetes (K8s)

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

3. Install sample microservice application:

   1. Robotshop: https://github.com/instana/robot-shop/blob/master/README.md
      
   2. QOTD: https://github.com/redhat-developer-demos/qotd/blob/master/README.md

4. Create a host file for the microservices:
   
      Example host file (hosts.ini):

            [local]

            localhost ansible_connection=local

            [k8s]

            ip-XXX-XX-X-XXX ansible_connection=local


4. Run the Ansible playbooks:
   
         ansible-playbook -i hosts.ini playbook.yml
   
## Usage of Dataset for Few-Shot Learning or In-context tuning

   To utilize the dataset for few-shot learning or in-context tuning of Large Language Models (LLMs), follow these steps:

   1. **Download the Dataset**: Obtain the dataset containing prompts in a text file and corresponding Ansible playbooks in YAML format. Ensure the file structure maintains a clear mapping between the prompts and their respective playbooks.
   2. **In-context-Tuning the LLM**: Use the provided prompts and corresponding Ansible playbooks for In-context-tuning your preferred LLM, such as GPT-4. You can use libraries like Hugging Face's 'transformers' to perform In-context-tuning. Follow the instructions provided by the library for In-context-tuning LLMs using your dataset. For example:
         
               Prompt:
               Write an Ansible playbook to retrieve a list of all deployments by running a shell command on Kubernetes nodes. Filter the results to only include the namespace and deployment name, and store them in two variables: 'deployment_name' and 'namespace'.
               
               Interference:
               prompt.txt
               
               Remediation code:
               ansible_playbook.yaml:
               ---
               - name: Retrieve list of deployments
                 hosts: k8s_nodes
                 tasks:
                   - name: Run shell command to get deployments

## Acknowledgments

We would like to thank and acknowledge the developers of Robot-shop and QOTD for their valuable contributions to the testing environment.


For more detailed instructions, refer to the paper[yet to publish).

## Citing KubePlaybook
Yet to publish

BibTex:
