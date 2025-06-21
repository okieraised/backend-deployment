## ☸️ Useful Kubernetes (kubectl) Commands

### 🔹 Installation
| Command                                                                     | Description                       |
|-----------------------------------------------------------------------------|-----------------------------------|
| `curl -sfL https://get.k3s.io \| INSTALL_K3S_EXEC="--disable traefik" sh -` | Install k3s with traefik disabled |

---

### 🔹 Cluster Info and Configuration

| Command | Description |
|--------|-------------|
| `kubectl config view` | Show merged kubeconfig settings |
| `kubectl config use-context <context>` | Switch between clusters |
| `kubectl cluster-info` | Show master and service endpoints |
| `kubectl get nodes` | List all nodes in the cluster |
| `kubectl describe node <node-name>` | Detailed node information |

---

### 🔹 Pod Management

| Command | Description |
|--------|-------------|
| `kubectl get pods` | List all pods in the current namespace |
| `kubectl get pods -A` | List all pods in all namespaces |
| `kubectl describe pod <pod>` | Detailed info about a pod |
| `kubectl logs <pod>` | View logs of a pod |
| `kubectl logs <pod> -c <container>` | View logs from a specific container |
| `kubectl exec -it <pod> -- /bin/bash` | Open shell inside a pod |
| `kubectl delete pod <pod>` | Delete a pod (it will be recreated if managed by a controller) |

---

### 🔹 Deployment & Service Management

| Command | Description |
|--------|-------------|
| `kubectl get deployments` | List deployments |
| `kubectl describe deployment <deployment>` | Detailed info about a deployment |
| `kubectl get svc` | List services |
| `kubectl get endpoints` | Show service endpoints |
| `kubectl rollout restart deployment <deployment>` | Restart a deployment |
| `kubectl scale deployment <deployment> --replicas=3` | Scale deployment to 3 replicas |
| `kubectl delete deployment <deployment>` | Delete a deployment |

---

### 🔹 Namespace Management

| Command | Description |
|--------|-------------|
| `kubectl get ns` | List all namespaces |
| `kubectl create namespace <name>` | Create a new namespace |
| `kubectl delete namespace <name>` | Delete a namespace |
| `kubectl config set-context --current --namespace=<ns>` | Set default namespace for current context |

---

### 🔹 YAML and Manifest Handling

| Command | Description |
|--------|-------------|
| `kubectl apply -f <file>.yaml` | Apply configuration from YAML |
| `kubectl delete -f <file>.yaml` | Delete resources from YAML |
| `kubectl create -f <file>.yaml` | Create resources from YAML |
| `kubectl edit <resource>/<name>` | Edit a resource in-place |
| `kubectl get <resource> <name> -o yaml` | Output resource as YAML |

---

### 🔹 Resource Types & Shortcuts

| Command | Description |
|--------|-------------|
| `kubectl get all` | Show all resource types |
| `kubectl api-resources` | List all supported resource types |
| `kubectl explain <resource>` | Get help and docs for a resource |
| Shortcuts: `po` = pod, `svc` = service, `deploy` = deployment, `ns` = namespace |

---

### 🔹 Troubleshooting

| Command | Description |
|--------|-------------|
| `kubectl describe <resource> <name>` | Show detailed info including events |
| `kubectl get events` | Show recent cluster events |
| `kubectl top pod` | Show pod resource usage (needs Metrics Server) |
| `kubectl get pod <pod> -o wide` | Show pod IP, node, etc. |
| `kubectl port-forward <pod> <local_port>:<pod_port>` | Forward local port to pod |

---

### 🔹 Context & Cluster Info

| Command | Description |
|--------|-------------|
| `kubectl config get-contexts` | Show all kubeconfig contexts |
| `kubectl config current-context` | Show current context |
| `kubectl config use-context <context>` | Switch to a different cluster context |

---
