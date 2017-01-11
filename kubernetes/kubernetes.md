# Deploy to Kubernetes

```bash
kubectl create -f kubernetes/slow-cooker.yaml
```

# View logs

```bash
kubectl logs $(oc get pods -lapp=slow-cooker -ojsonpath={..metadata.name})
```

# Remove from Kubernetes

```bash
kubectl delete rc slow-cooker
```

# Debugging

## Shell access

```bash
kubectl exec -it $(oc get pods -lapp=slow-cooker -ojsonpath={..metadata.name}) bash
```
