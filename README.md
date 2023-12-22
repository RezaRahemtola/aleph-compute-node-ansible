# Deploy Aleph.im CRNs with Ansible 💻

Easily create, update or redeploy [Aleph.im Compute Resource Nodes](https://docs.aleph.im/nodes/compute/) on Ubuntu 22.04 using Ansible 🚀

## Getting started ✨

- [Install Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)
- Create an `inventory.ini` file with the following format:
```ini
[compute_hosts]
username@IP domain=vm.example.org
username@IP2 domain=vm2.example.org

[compute_hosts:vars]
node_version=0.3.1
```
- Launch the playbook:
```sh
ansible-playbook -i inventory.ini playbook.yaml
```
- Add DNS records on your domain that point to the server on IPv4 (A) and IPv6 (AAAA)

**Check on `https://YOUR_DOMAIN` that everything works correctly 🔥**

Tested successfully with:
- [Scaleway instances](https://www.scaleway.com/en/virtual-instances/)

> ⚠️ This is a work in progress and currently only covers basic cases.\
> If this doesn't work with your provider, please refer to the [official documentation](https://docs.aleph.im/nodes/compute/installation/ubuntu-22.04).
