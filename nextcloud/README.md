# Nextcloud deployment using Helm

## Deploy

helm install --name nextcloud stable/nextcloud --values=https://raw.githubusercontent.com/ciseldevops/k8s/master/nextcloud/values.yaml

## Upgrade
helm upgrade nextcloud stable/nextcloud --values=https://raw.githubusercontent.com/ciseldevops/k8s/master/nextcloud/values.yaml  --set nextcloud.password=******,nextcloud.host=nextcloud.example.com

## Validate
nextcloudk8sdev.cisel.lan

## Clean
helm list

helm delete --purge nextcloud
