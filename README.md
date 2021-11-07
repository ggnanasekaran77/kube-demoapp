# kube-demoapp
```
gcloud container clusters get-credentials cluster-1 --zone asia-southeast1-a --project my-second-project-329918 \
 && kubectl port-forward --namespace argocd $(kubectl get pod --namespace argocd --selector="app.kubernetes.io/name=argocd-server" --output jsonpath='{.items[0].metadata.name}') 8080:8080

 kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
 ```
