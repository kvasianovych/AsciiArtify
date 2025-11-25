# AsciiArtify

## Kubernetes Tool Set Comparison for Local Development

1. ### minikube
   Official Kubernetes project that creates a local Kubernetes cluster on your machine. It runs a single-node or multi-node cluster inside a VM, container, or bare-metal, making it ideal for learning Kubernetes and local development.

   #### Supported OSes:
   - Linux
   - MacOS
   - Windows

   #### Supported Architectures:
   - x86-64 (amd64)
   - ARM64
   - ARMv7
   - ppc64le
   - S390x

   #### Feature list:
   - Supports multiple container runtimes (Docker, containerd, CRI-O)
   - Multiple driver options (Docker, Podman, VirtualBox, VMware, Hyper-V, KVM)
   - Built-in addons system (dashboard, metrics-server, ingress, etc.)
   - LoadBalancer emulation via minikube tunnel
   - Multi-node cluster support
   - Registry support with easy image loading
   - Integrated dashboard access

2. ### k3s
   Lightweight wrapper that runs k3s (Rancher's minimal Kubernetes distribution) in Docker containers. It's designed for creating multi-node clusters quickly and efficiently, with minimal resource overhead.

   #### Supported OSes:
   - Linux
   - MacOS
   - Windows

   #### Supported Architectures:
   - x86-64 (amd64)
   - ARM64

   #### Feature list:
   - Fast cluster creation (typically under 30 seconds)
   - Multi-node cluster support (multiple masters and workers)
   - Built-in load balancer for exposed services
   - Easy port mapping from cluster to host
   - Volume mounting support
   - Image import from local Docker
   - Registry creation and management
   - Automatic kubeconfig management

3. ### kind
   (Kubernetes IN Docker) was primarily created for testing Kubernetes itself but has become popular for local development. It runs Kubernetes clusters using Docker containers as nodes, offering a balance between simplicity and feature completeness.

   #### Supported OSes:
   - Linux
   - MacOS
   - Windows

   #### Supported Architectures:
   - x86-64 (amd64)
   - ARM64

   #### Feature list:
   - Multi-node cluster support
   - Runs entirely in Docker containers
   - Extrapolated port mappings
   - Custom node images support
   - Local registry integration
   - Ingress support via configuration
   - Originally designed for CI/CD testing
   - Declarative cluster configuration via YAML

### Comparison Table
| Aspect | Minikube | k3d | kind |
| :-- | :-- | :-- | :-- |
| Ease of Use | Easiest to set up, beginner-friendly | Moderately easy, balances ease \& flexibility | More control needed, less beginner-friendly |
| Deployment Speed | Slower due to VM overhead | Very fast due to container-based k3s | Fast, container-based |
| Stability | Stable and mature | Stable, lightweight production-grade k3s base | Stable, reliable for testing |
| Documentation \& Support | Extensive official docs and community | Growing community, good docs | Good documentation, strong community |
| Configuration Complexity | Simple, but some driver options can be complex | Moderate | Can be complex, especially for multi-node setups |
| Resource Usage | Higher resource usage due to VM | Low resource usage | Low resource usage |
| Cluster Type | Primarily single-node, multi-node possible | Multi-node supported | Multi-node supported |
| Use Case Suitability | Learning, simple development | Lightweight local dev, CI/CD, rapid testing | CI/CD, network testing, complex dev setups |

## K8S Demos
### Minikube
![minikube](../media/minikube.gif)
### k3d
![k3d](../media/k3d.gif)
### kind
![kind](../media/kind.gif)

## App Demo
### AsciiArtify
![AsciiArtify-Demo](../media/w4argo.gif)
