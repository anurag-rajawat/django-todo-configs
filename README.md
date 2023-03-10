# django-todo-configs
This repository hosts the configuration for django [todo app](https://github.com/anurag-rajawat/django-todo)

The goal is to configure web server to run our app using [Ansible](https://www.ansible.com)

# 🚀 Getting Started
- Create a ubuntu web-server instance on any cloud provider
- Allow HTTP (port 80) traffic on your instance
- Update instance details in [hosts](inventory/hosts) file
- Execute [docker](playbooks/docker.yml) playbook to install docker on instance

    ```shell
    $ ansible-playbook playbooks/docker.yml
    ```
- Execute [app](playbooks/app.yml) playbook to start app on instance

    ```shell
    $ ansible-playbook playbooks/app.yml
    ```
- Open `http://<server_public_ip_address>` in your favorite browser

# 🛠️ Troubleshooting

- CORS policy related
  - For chrome, disable `Block insecure private network requests` flag, to do so head over to `chrome://flags/#block-insecure-private-network-requests`
  wait 2-3 minutes and try again.
