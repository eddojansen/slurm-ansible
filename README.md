# slurm-ansible
Step1: Edit the inventory list to match the master and slave nodes in your environment.
Step2: Edit the var/slurm.yaml file to match the resources of your environment.
Step3: Install ansible on the master node with apt/yum install ansible -y (or use another ansible host)
Step4: Ensure that ssh keys are configured for passwordless access and sudo
Step5: Deploy slurm cluster by running ansible playbook with:
       ansible-playbook -i inventory install-slurm.yaml -vvvv (v for verbosity)
       
Step6: Remove and cleanup installation by running the cleanup-slurm.yaml playbook:
       ansible-playbook -i inventory cleanup-slurm.yaml
