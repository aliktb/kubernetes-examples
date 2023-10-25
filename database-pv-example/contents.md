# Contents

- Persistent volume (PV) - defined to allocate stoarge from local backend (could be replaced with remote (e.g. NFS) or cloud (e.g. AWS Block Storage)). Usually set by admin
- Persistent Volume Claim (PVC) - claiming a PV for use by a specific application. Usually set by developer
- Deployment - Deployment of postgres database with 1 replicaSet for demo purposes
- Service - Exposing DB deployment
