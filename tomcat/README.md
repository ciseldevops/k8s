## Deploy Tomcat using Helm
kubectl create -f tomcat-ingress.yaml
helm install --name tomcat -f values.yaml stable/tomcat 

## Validate
http://tomcatk8sdev.cisel.lan/sample/

## Infos
kubectl exec -it tomcat -- /bin/bash
ls -al /usr/local/tomcat/webapps
