# Nextcloud deployment using Helm

kubectl create -f nextcloud-ingress.yaml

helm install --name nextcloud stable/nextcloud

helm upgrade nextcloud stable/nextcloud --set nextcloud.host=nextcloud.example.com

kubectl get service

kubectl get pods
