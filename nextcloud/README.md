# Nextcloud deployment using Helm

## Deploy
kubectl create -f nextcloud-ingress.yaml

Basic install:
helm install --name nextcloud -f values.yaml stable/nextcloud

Advanced install:
helm install --name nextcloud -f values.yaml stable/nextcloud --set nextcloud.password=******,nextcloud.host=nextcloud.example.com

## Tune
helm upgrade nextcloud -f values.yaml stable/nextcloud --set nextcloud.password=******,nextcloud.host=nextcloud.example.com

## Validate
kubectl get service

kubectl get pods

http://nextcloud.example.com
