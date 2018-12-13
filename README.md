## what is kube-build

kube-build is a tool that help you to build the kubernetes compiling environment (golang 1.11), support

- kubeadm
- kube-apiserver
- kube-scheduler
- kube-proxy
- kube-controller-manager
- kube-controller


## how to use kube-build

### 1 build it

```
cd build-image
docker build -t shidaqiu/kube-build:latest .
```

### 2 get it form DockerHub

2.1. download kube-build

```
docker pull shidaqiu/kube-build
```

2.2. run kube-build, then you are inside the container

```
docker run -it -v [k8s.io location]:/usr/lib/go/src/k8s.io shidaqiu/kube-build
```

2.3. for example, if we want to build kubeadm, we can execute the following commands inside the container

```
cd /usr/lib/go/src/k8s.io/kubernetes/cmd/kubeadm
go build
```
