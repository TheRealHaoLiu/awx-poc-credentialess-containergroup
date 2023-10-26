# awx-poc-credentialess-containergroup

Create container group in AWX outside of the namespace that AWX is deployed in WITHOUT needing to provide a Credential

## Required Environment Varibale

- CONTROLLER_HOST: hostname of the AWX API
- CONTROLLER_USERNAME: username of the AWX instance
- CONTROLLER_PASSWORD: password for the AWX user

- K8S_AUTH_KUBECONFIG: kubeconfig file for the K8S cluster where AWX is deployed on

## Playbook vars

- awx_name: name of the AWX resource
- awx_namespace: namespace where AWX is deployed in
- container_group_namespace: namespace that you want the container group to target

## Running the playbook

```bash
ansible-playbook create_container_group.yml
```
