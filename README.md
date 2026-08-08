# Pihole Automation

Set of ansible scripts used to maintain pihole.

Requires Ansible installed on the contorl node (machine you're running the playbooks from).

## Generate SSH Keys

Set up SSH key auth so Ansible can connect without password

```bash
# Generate a key pair (skip if you already have one, e.g. ~/.ssh/id_ed25519)
ssh-keygen -t ed25519 -C "ansible-pihole"

# Copy the public key to each Pi-hole host
ssh-copy-id admin@piholeXX
```

## Running playbooks

```bash
ansible-playbook -i inventory.yml update-pihole.yml
```
