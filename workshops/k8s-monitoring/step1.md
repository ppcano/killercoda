# Things to know

Before you begin, here are some things you should know:

- **Loki**: Loki can run in a single binary mode or as a distributed system. In this tutorial, we will deploy Loki as a single binary otherwise known as monolithic mode. Loki can be vertically scaled in this mode depending on the amount of logs you are collecting. It is recommended to run Loki in a distributed/microservice mode for production use cases to monitor high volumes of logs.

- **Deployment**: We will deploy Loki, Grafana and Alloy (As part of the Kubernetes Monitoring Helm) in the `meta`{{copy}} namespace of your Kubernetes cluster. Make sure you have the necessary permissions to create resources in this namespace. These pods will also require resources to run so consider the amount of capacity your nodes have available. It also possible to just deploy the Kubernetes monitoring helm (since it has a minimal resource footprint) within your cluster and write logs to an external Loki instance or Grafana Cloud.

- **Storage**:  In this tutorial, Loki will use the default object storage backend provided in the Loki Helm; [MinIO](https://min.io/docs/minio/kubernetes/upstream/index.html). You should migrate to a more production-ready storage backend like [S3](https://aws.amazon.com/s3/getting-started/), [GCS](https://cloud.google.com/storage/docs), [Azure Blob Storage](https://learn.microsoft.com/en-us/azure/storage/blobs/) or a MinIO Cluster for production use cases.

# Killercode Prerequisites

Hola PortuGrots!!!

Information unique to Killercoda
