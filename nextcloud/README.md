# Nextcloud deployment using Helm

## Deploy
kubectl create -f nextcloud-ingress.yaml

helm install --name nextcloud -f values.yaml stable/nextcloud

## Tune
helm upgrade nextcloud -f values.yaml stable/nextcloud --set nextcloud.password=MYNEWPASSWORD,nextcloud.host=nNEXTCLOUD.EXAMPLE.COM

## Validate
kubectl get service

kubectl get pods

http://nextcloud.example.com
