# Nextcloud deployment using Helm

## Deploy
kubectl create -f nextcloud-ingress.yaml

helm install --name nextcloud -f values.yaml stable/nextcloud

## Tune
helm upgrade nextcloud stable/nextcloud --set nextcloud.host=nextcloud.example.com

## Validate
kubectl get service

kubectl get pods

http://nextcloud.example.com
