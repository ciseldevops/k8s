# Nextcloud deployment using Helm

Deploy Nextcloud using Helm
kubectl create -f nextcloud-ingress.yaml
helm install --name nextcloud stable/nextcloud
helm upgrade nextcloud stable/nextcloud --set nextcloud.host=nextcloudk8sdev.cisel.lan

kubectl get service
kubectl get pods
