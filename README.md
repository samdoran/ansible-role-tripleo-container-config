TripleO Container Config
=========

Run a container and generate config files using the Ansible playbooks inside the container. The generate config will be saved in the project directory for later use.

Requirements
------------

A container runtime must be installed. Docker and Podman are supported.

Role Variables
--------------

| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `ooo_cc_container_runtime` | `docker` | Container runtime to use. Podman and Docker are supported. |
| `ooo_cc_containers` | `[]` | List of containers to run and their settings. See `defaults/main.yml` for examples. |
| `ooo_cc_config_path` | `{{ playbook_dir }}/generated_config` | Directory where generated configs are saved. |


Dependencies
------------

`docker-py` for Docker
`podman` for Podman

Example Playbook
----------------

    - hosts: all
      roles:
         - openstack.tripleo-container-config

License
-------

Apache 2.0
