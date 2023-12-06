# dockt-cbd3345-ansible
Ansible Repository to maintain the desired state of the system
​
## Structure
​
```
doct-cbd3345-ansible/
├── .github/
│   └── workflows/                  # GitHub Actions Workflows
│       ├── add-ssh-users.yml       # The workflow to run add ssh keys Playbook
│       ├── host-preparation.yml    # The workflow to run host preparation Playbook
│       ├── upgrade-java.yml        # The workflow to run upgrade java Playbook
│       └── ...
├── inventories/                    # Ansible Inventories
│   ├── productions/                # Production Environment Inventory
│   └── staging/                    # User Acceptance Test Environment Inventory
│   └── ...
├── playbooks/                      # Ansible Inventories
│   ├── add_ssh_keys.yml            # The Playbook to add public keys of users who can SSH to the server
│   ├── host_preparation.yml        # The Playbook to configure security hardening and install packages
│   ├── upgrade_java.yml            # The Playbook to upgrade java version on the server
│   └── ...
├── shared_vars/                    # Shared Variables that can be used in Playbooks
│   ├── team_pub_keys_secret.yml    # The encrypted public keys of users to use in the Playbook
│   ├── vault_keyfile               # This key is not uploaded to the repository but maintain within team locally
│   └── ...
├── .gitignore                      # Excluded Files List for Git
├── README.md                       # This readme file
└── ...
```
