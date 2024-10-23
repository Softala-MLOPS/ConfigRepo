# ConfigRepo
This is the configuration repo

Requirements
pip install pyyaml
pip install typer
(type -p wget >/dev/null || (sudo apt update && sudo apt-get install wget -y)) \
	&& sudo mkdir -p -m 755 /etc/apt/keyrings \
	&& wget -qO- https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo tee /etc/apt/keyrings/githubcli-archive-keyring.gpg > /dev/null \
	&& sudo chmod go+r /etc/apt/keyrings/githubcli-archive-keyring.gpg \
	&& echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null \
	&& sudo apt update \
	&& sudo apt install gh -ys


setup_cli.py config.yaml file example:
```plaintext 
    KUBEFLOW_ENDPOINT: http://localhost:8080
    KUBEFLOW_USERNAME: user@example.com
    KUBEFLOW_PASSWORD: '12341234'
    REMOTE_CSC_CLUSTER_SSH_PRIVATE_KEY: ''
    REMOTE_CSC_CLUSTER_SSH_IP: ''
    REMOTE_CSC_CLUSTER_SSH_USERNAME: ''
```