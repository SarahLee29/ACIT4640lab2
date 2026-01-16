# ACIT4640lab2

## Part 3

create and go to the target loaction:

`mkdir -p part1-scripts`

` cd part1-scripts/`

create the environment variable file:

`nano env-vars.sh`

### script 1

create the script 1 file:

` nano nginx-install.sh`

write the following commands:

```
#!/bin/bash

source ./env_vars.sh

ssh -i "$SSH_KEY_PATH" "$USERNAME@$IP_ADDRESS" <<  'EOF'
sudo apt update
sudo apt install -y nginx
sudo systemctl start nginx
sudo systemctl enable ngin
EOF
```

1. Inside the script, firstly *source* to `env_vars.sh` so that the variable defined in that file can be used in the script.

2. Then `ssh` is used to connect to EC2 instance.

3. Finanlly, updating the package management, installing nginx, enabling it, are setting up sequencially.

### script 2
create the script 2 file:
`nano document-write.sh`



