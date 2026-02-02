Kubernetes Volumes, PV & PVC
This repository demonstrates how Kubernetes handles storage using Volumes, Persistent Volumes (PV), and Persistent Volume Claims (PVC).

Why Storage is Needed in Kubernetes
Pods and containers are ephemeral
Pods can restart, be deleted, or move between nodes
Without external storage, data is lost
Kubernetes solves this using persistent storage abstractions.

Core Concepts
Volume
Defined inside a Pod
Provides storage to containers
Exists only for the lifetime of the Pod
Not persistent across Pod deletion
Persistent Volume (PV)
Cluster-level storage resource
Backed by real storage (disk, cloud, NFS, etc.)
Independent of Pods
Data survives Pod restarts and recreation
Persistent Volume Claim (PVC)
A request for storage made by applications
Automatically binds to a matching PV
Abstracts storage implementation details
Relationship Between PV, PVC, and Pod
PV → PVC → Pod → Container

PV owns the storage
PVC claims the storage
Pod mounts the storage
Container reads/writes data
