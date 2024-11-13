# Kubernetes Client-Go Example

This project demonstrates the usage of the official Kubernetes Go client (client-go) to interact with a Kubernetes cluster. It includes examples of:
- Connecting to a Kubernetes cluster using kubeconfig
- Listing pods across all namespaces
- Demonstrating error handling when getting pod information

## Prerequisites

- Go 1.16 or higher
- Access to a Kubernetes cluster
- Kubeconfig file configured with cluster access

## Dependencies

The project uses the following main dependencies:
- k8s.io/client-go
- k8s.io/apimachinery

## Building and Running

1. Clone the repository:
```bash
git clone <repository-url>
cd k8s-crud-clientgo
```

2. Install dependencies:
```bash
go mod tidy
```

3. Run the application:
```bash
go run main.go
```

By default, the application will:
- Use your default kubeconfig file (~/.kube/config)
- List all pods in the cluster every 10 seconds
- Attempt to find a pod named "example-xxxxx" in the default namespace

## Configuration

You can specify a custom kubeconfig file location using the `-kubeconfig` flag:

```bash
go run main.go -kubeconfig=/path/to/your/kubeconfig
```

## Features

1. **Cluster Connection**: Establishes connection to a Kubernetes cluster using local kubeconfig
2. **Pod Listing**: Periodically lists all pods in the cluster
3. **Error Handling**: Demonstrates proper error handling for Kubernetes API operations

## License

[Add your license information here]