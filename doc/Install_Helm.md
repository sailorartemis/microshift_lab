## Helm

### Install

Install via script
```bash
curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-4
chmod 700 get_helm.sh
./get_helm.sh
helm version
```

Enable shell completion
```bash
helm completion bash | sudo tee /etc/bash_completion.d/helm
source ~/.bashrc
```

