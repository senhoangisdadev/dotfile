# Dotfiles - Docker & Kubernetes Alias Collection

This repository contains useful aliases for Docker, Docker Compose, and Kubernetes, making it easier to manage containers and services on your server.

## 🚀 Features

- Common Docker aliases
- Common Docker Compose aliases
- Common Kubernetes aliases (Single Node)
- Easy synchronization between machines via Git
- Time-saving container management on servers

## 📋 Installation Steps

1. Clone this repository to your local machine:
```bash
git clone https://github.com/YOUR_USERNAME/dotfiles.git
cd dotfiles
```

2. Create a symbolic link from the alias file in the repo to your home directory:
```bash
ln -s $(pwd)/.aliases ~/.aliases
```

3. Add the following line to your `~/.zshrc` or `~/.bashrc`:
```bash
if [ -f ~/.aliases ]; then
    source ~/.aliases
fi
```

4. Reload shell configuration:
```bash
source ~/.zshrc  # for zsh
# or
source ~/.bashrc # for bash
```

## 🐳 Alias List

### Docker Aliases

| Alias | Command | Description |
|-------|---------|-------------|
| d | docker | Shorthand for docker command |
| di | docker images | List all images |
| dps | docker ps | List running containers |
| dpsa | docker ps -a | List all containers |
| drm | docker rm | Remove container |
| drmi | docker rmi | Remove image |
| dex | docker exec -it | Access container shell |
| dlogs | docker logs -f | View container logs |

### Docker Compose Aliases

| Alias | Command | Description |
|-------|---------|-------------|
| dc | docker-compose | Shorthand for docker-compose |
| dcu | docker-compose up | Start services |
| dcud | docker-compose up -d | Start services in background |
| dcd | docker-compose down | Stop and remove containers, networks |
| dcr | docker-compose restart | Restart services |
| dcl | docker-compose logs -f | View service logs |

### Kubernetes Aliases

| Alias | Command | Description |
|-------|---------|-------------|
| k | kubectl | Shorthand for kubectl |
| kgp | kubectl get pods | View list of pods |
| kgpa | kubectl get pods --all-namespaces | View pods in all namespaces |
| kgd | kubectl get deployments | View list of deployments |
| kgs | kubectl get services | View list of services |
| kgn | kubectl get nodes | View list of nodes |
| kgns | kubectl get namespaces | View list of namespaces |
| kdp | kubectl describe pod | View pod details |
| kdd | kubectl describe deployment | View deployment details |
| kds | kubectl describe service | View service details |
| kdn | kubectl describe node | View node details |
| kl | kubectl logs -f | View pod logs |
| kex | kubectl exec -it | Access pod shell |
| kaf | kubectl apply -f | Apply resource from file |
| kdf | kubectl delete -f | Delete resource from file |
| krm | kubectl delete | Delete resource |
| kroll | kubectl rollout restart deployment | Restart deployment |
| krollh | kubectl rollout history deployment | View rollout history |
| krollu | kubectl rollout undo deployment | Rollback deployment |

#### Context and Namespace Management

| Alias | Command | Description |
|-------|---------|-------------|
| kgc | kubectl config get-contexts | View list of contexts |
| kuc | kubectl config use-context | Switch context |
| kcc | kubectl config current-context | View current context |
| kns | kubectl config set-context --current --namespace | Change default namespace |

#### Monitoring and Debugging

| Alias | Command | Description |
|-------|---------|-------------|
| ktop | kubectl top pods | View pod resources |
| ktopn | kubectl top nodes | View node resources |
| kpf | kubectl port-forward | Forward port from pod |
| kevents | kubectl get events | View time-sorted events |

## 📋 System Requirements

- Docker and Docker Compose installed
- Kubernetes (kubectl) installed
- Git

## 🔄 Updates and Synchronization

1. When making local changes:
```bash
git add .
git commit -m "Update aliases"
git push origin main
```

2. To sync on a new server:
```bash
git clone https://github.com/YOUR_USERNAME/dotfiles.git
cd dotfiles
# Follow installation steps as above
```

## 🤝 Contributing

All contributions are welcome! Please create a pull request to add more useful aliases.

## 📝 License

MIT License 