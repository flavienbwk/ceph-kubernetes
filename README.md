# Ceph Kubernetes

A repo-tutorial to learn how to install and use Ceph on a Kubernetes cluster (block storage).

## What

Ceph is an open-source software-defined storage solution which allows you to store data as object (Ceph Object Gateway - S3-compatible), block (Ceph OSD) or file (CephFS).

What we will be doing :

1. Install Ceph on a 3-nodes Kubernetes cluster
2. Deploy a web service that creates and exposes 3 files
3. Stop the Kubernetes node on which our web service is deployed
4. See what happens (but will be re-scheduled, but has our block storage lost data ?)

{Image}

## Why

Data access without a single point of failure.

Ceph is {Fault-tolerant replicated storage for any block storage (databases, apps)}

Additionnaly, think avoiding putting more disks into your current server. Avoid saturating I/O too. {Save money by lowering maintenance cost of storage servers as it is managed by Kubernetes (updates across the cluster, horizontal scaling on several smaller servers) | disaster recovery}

With Ceph, you have a [continuous scaling path, forward, forever](https://www.youtube.com/watch?v=yeAlzSp6yaE).
