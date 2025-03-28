# Bootstrapping the Overlay router

## Prerequisites

- Install sshpass on the ansible controller that is used to bootstrap the overlay routers.
  
```bash
$ brew install sshpass
```

- Check the connectivity to the machines
  
```bash
$ ansible -i inventory -m ping routers
10.232.80.168 | SUCCESS => {
    "ansible_facts": {
        "discovered_interpreter_python": "/usr/bin/python3.10"
    },
    "changed": false,
    "ping": "pong"
}
10.232.80.132 | SUCCESS => {
    "ansible_facts": {
        "discovered_interpreter_python": "/usr/bin/python3.10"
    },
    "changed": false,
    "ping": "pong"
}
```

```bash
$ ansible-playbook -i inventory main.yaml
```