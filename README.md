# K8s-Webinar-Storage-Persistent
Host-Based Volume - and - NFS-Based Volume + PV and PVC


## Code from Kubernetes Webinar Series - Dealing with Storage and Persistence
https://www.youtube.com/watch?v=n06kKYS6LZE

## Narrative for this demo
1. Host-Based Volume

2. NFS-Based Volume + PV and PVC




## Deploy the app to Kubernetes - Host-Based Volume
```
cd ../Deploy-Kubernetes/Host-Based-Vol
kubectl create -f pod-vol-local.yml
```

## Check mounted volume on POD corresponds to Host local volume:
POD mounted volume: /usr/share/nginx/html
Host local volume: /var/lib/my-data



## Deploy the app to Kubernetes - NFS-Based Volume + PV and PVC
```
cd ../Deploy-Kubernetes/NFS-Based-Vol-PV-PVC
kubectl create -f my-pv.yml
kubectl create -f my-pvc.yml
kubectl create -f my-pod.yml
```

## Check mounted volume on POD corresponds to NFS shared volume:
POD mounted volume: /usr/share/nginx/html
NFS shared volume: /DATA/NFS/web

