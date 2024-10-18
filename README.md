# Kubernetes Edge-Cloud Continuum Dataset

This repository contains a collection of synthetically generated datasets that model Kubernetes nodes and pods across the edge-cloud continuum.

## Dataset Structure

Each dataset is organized into folders, named according to the following pattern:

```
<number_of_nodes>_nodes_<target_utilization_percentage>_util_<instance_id>
```

- **`<number_of_nodes>`**: The total number of Kubernetes nodes in the continuum.
- **`<target_utilization_percentage>`**: The target utilization of the nodes, expressed as a percentage (e.g., 70 for 70%).
- **`<instance_id>`**: A unique identifier for the dataset instance.

### Folder Contents

Each folder contains the following files:

- **`nodes.csv`**: A CSV file containing information about the nodes, including their resource capacities (CPU, memory, etc.) and metadata. The header comments describe the parameters used to generate the dataset.
- **`node-latencies.json`**: A JSON file that provides latency data between nodes within the same cluster (intra-cluster latencies) and between nodes in different clusters (inter-cluster latencies).
- **`pods.csv`**: A CSV file containing resource requests and metadata for the pods. Like `nodes.csv`, the header comments explain the parameters used in dataset generation.
- **`workload-latency-requests.json`**: A JSON file specifying the latency requests between different workloads.
