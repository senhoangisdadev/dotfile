# Dotfiles - Docker & Kubernetes Alias Collection

Repository này chứa các alias hữu ích cho Docker, Docker Compose và Kubernetes, giúp quản lý container và services dễ dàng hơn trên server.

## 🚀 Tính năng

- Các alias phổ biến cho Docker
- Các alias phổ biến cho Docker Compose
- Các alias phổ biến cho Kubernetes (Single Node)
- Dễ dàng đồng bộ giữa các máy thông qua Git
- Tiết kiệm thời gian khi làm việc với container trên server

## 📋 Các bước cài đặt

1. Clone repository này về máy local:
```bash
git clone https://github.com/YOUR_USERNAME/dotfiles.git
cd dotfiles
```

2. Tạo symbolic link từ file alias trong repo đến thư mục home:
```bash
ln -s $(pwd)/.aliases ~/.aliases
```

3. Thêm dòng sau vào file `~/.zshrc` hoặc `~/.bashrc`:
```bash
if [ -f ~/.aliases ]; then
    source ~/.aliases
fi
```

4. Reload shell configuration:
```bash
source ~/.zshrc  # nếu dùng zsh
# hoặc
source ~/.bashrc # nếu dùng bash
```

## 🐳 Danh sách Alias

### Docker Aliases

| Alias | Command | Mô tả |
|-------|---------|--------|
| d | docker | Rút gọn lệnh docker |
| di | docker images | Liệt kê các images |
| dps | docker ps | Liệt kê các container đang chạy |
| dpsa | docker ps -a | Liệt kê tất cả container |
| drm | docker rm | Xóa container |
| drmi | docker rmi | Xóa image |
| dex | docker exec -it | Truy cập vào container |
| dlogs | docker logs -f | Xem logs của container |

### Docker Compose Aliases

| Alias | Command | Mô tả |
|-------|---------|--------|
| dc | docker-compose | Rút gọn lệnh docker-compose |
| dcu | docker-compose up | Khởi động services |
| dcud | docker-compose up -d | Khởi động services trong background |
| dcd | docker-compose down | Dừng và xóa containers, networks |
| dcr | docker-compose restart | Khởi động lại services |
| dcl | docker-compose logs -f | Xem logs của services |

### Kubernetes Aliases

| Alias | Command | Mô tả |
|-------|---------|--------|
| k | kubectl | Rút gọn lệnh kubectl |
| kgp | kubectl get pods | Xem danh sách pods |
| kgpa | kubectl get pods --all-namespaces | Xem pods ở tất cả namespaces |
| kgd | kubectl get deployments | Xem danh sách deployments |
| kgs | kubectl get services | Xem danh sách services |
| kgn | kubectl get nodes | Xem danh sách nodes |
| kgns | kubectl get namespaces | Xem danh sách namespaces |
| kdp | kubectl describe pod | Xem chi tiết pod |
| kdd | kubectl describe deployment | Xem chi tiết deployment |
| kds | kubectl describe service | Xem chi tiết service |
| kdn | kubectl describe node | Xem chi tiết node |
| kl | kubectl logs -f | Xem logs của pod |
| kex | kubectl exec -it | Truy cập vào pod |
| kaf | kubectl apply -f | Apply resource từ file |
| kdf | kubectl delete -f | Xóa resource từ file |
| krm | kubectl delete | Xóa resource |
| kroll | kubectl rollout restart deployment | Restart deployment |
| krollh | kubectl rollout history deployment | Xem lịch sử rollout |
| krollu | kubectl rollout undo deployment | Rollback deployment |

#### Quản lý Context và Namespace

| Alias | Command | Mô tả |
|-------|---------|--------|
| kgc | kubectl config get-contexts | Xem danh sách contexts |
| kuc | kubectl config use-context | Chuyển đổi context |
| kcc | kubectl config current-context | Xem context hiện tại |
| kns | kubectl config set-context --current --namespace | Đổi namespace mặc định |

#### Monitoring và Debugging

| Alias | Command | Mô tả |
|-------|---------|--------|
| ktop | kubectl top pods | Xem tài nguyên của pods |
| ktopn | kubectl top nodes | Xem tài nguyên của nodes |
| kpf | kubectl port-forward | Forward port từ pod |
| kevents | kubectl get events | Xem events được sắp xếp theo thời gian |

## 📋 Yêu cầu hệ thống

- Docker và Docker Compose đã được cài đặt
- Kubernetes (kubectl) đã được cài đặt
- Git

## 🔄 Cập nhật và Đồng bộ

1. Khi có thay đổi trên local:
```bash
git add .
git commit -m "Update aliases"
git push origin main
```

2. Để đồng bộ trên server mới:
```bash
git clone https://github.com/YOUR_USERNAME/dotfiles.git
cd dotfiles
# Thực hiện các bước cài đặt như trên
```

## 🤝 Đóng góp

Mọi đóng góp đều được chào đón! Hãy tạo pull request để thêm các alias hữu ích khác.

## 📝 License

MIT License 