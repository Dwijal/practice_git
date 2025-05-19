## Kubernetes Persistent Storage Commands Cheat Sheet

---

### Persistent Volume (PV)

```bash
# Copy file from local to pod volume
kubectl cp ./local-file.txt <namespace>/<pod-name>:/mnt/volume

# Copy file from pod volume to local
kubectl cp <namespace>/<pod-name>:/mnt/volume/file.txt ./local-dir

# To check the pod  disk space/file system use the below command

grep -v rootfs  /proc/mounts >  /etc/mtab


# List all Persistent Volumes
kubectl get pv

# Describe a specific PV
kubectl describe pv <pv-name>

# Delete a PV
kubectl delete pv <pv-name>


# List all PVCs in the current namespace
kubectl get pvc

# List PVCs in a specific namespace
kubectl get pvc -n <namespace>

# Describe a specific PVC
kubectl describe pvc <pvc-name>

# Delete a PVC
kubectl delete pvc <pvc-name>


