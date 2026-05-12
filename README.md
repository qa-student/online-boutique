# online-boutique

# Automated Deployment
1. In Harness, run the online-boutique pipeline
2. Get the pods in your namespace:

kubectl get pods -n lbg-trainer

3. Get the external IP of the frintend service:

kubectl get service frontend-external -n lbg-trainer

4. Use http not https to browse the Online Boutique

##################################################################

# Manual Setup
1. connect to prod cluster:
gcloud container clusters get-credentials lbg-gke --region europe-west1 --project lbg-mea-leaders-c41

2. apply the k8s manifest
kubectl apply -f ./release/kubernetes-manifests.yaml

3. wait for pods to be ready
kubectl get pods

4. get svc external ip
kubectl get service frontend-external


5. use http not https to browse the Online Boutique

#################################################################


