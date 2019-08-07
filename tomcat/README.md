## Description
Déploiement d'une application Tomcat de démo "Hello World"

## Install
kubectl create -f https://raw.githubusercontent.com/ciseldevops/k8s/master/tomcat/tomcat-ingress.yaml

helm install --name tomcat --values=https://raw.githubusercontent.com/ciseldevops/k8s/master/tomcat/values.yaml stable/tomcat  --set tomcat.hosts=tomcatk8sdev.cisel.lan

## Tests et accès
http://tomcatk8sdev.cisel.lan/sample/

## Upgrade/Resize
Modifier le fichier yaml : 
 - le tag du repository correspond à la version. Il peut être changé pour atteindre une nouvelle version
 - replicaCount correspond au nombre de pods. Il peut être changé pour atteindre un nouveau nombre de réplicats
helm upgrade tomcat stable/tomcat --values=https://raw.githubusercontent.com/ciseldevops/k8s/master/tomcat/values.yaml

## Clean
helm list
helm delete tomcat --purge

## Infos
kubectl exec -it tomcat -- /bin/bash
ls -al /usr/local/tomcat/webapps
