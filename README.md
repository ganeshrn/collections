# collections
Network collections redirection

Steps to test:
1) Update routing.yml in `lib/ansible/config/rotuing.yml`

```
plugin_routing:
  connection:
    network_cli:
      redirect: ansible.netcommon.network_cli
    persistent:
      redirect: ansible.netcommon.persistent
  terminal:
    eos:
      redirect: arista.eos.eos
  cliconf:
    eos:
      redirect: arista.eos.eos
  modules:
    eos_acl_interfaces:
      redirect: arista.eos.eos_acl_interfaces
```


2) Clone the repository

```
git clone https://github.com/ganeshrn/collections.git
cd collections
```

3) Update inventory file

4) Run test

```
ansible-playbook redirect_test.yml -vvvvv
```
