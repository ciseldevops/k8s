## Deploy Tomcat using Helm
kubectl create -f https://raw.githubusercontent.com/ciseldevops/k8s/master/tomcat/tomcat-ingress.yaml

helm install --name tomcat --values=https://raw.githubusercontent.com/ciseldevops/k8s/master/tomcat/values.yaml stable/tomcat  --set tomcat.hosts=tomcatk8sdev.cisel.lan

## Validate
http://tomcatk8sdev.cisel.lan/sample/

## Infos
kubectl exec -it tomcat -- /bin/bash
ls -al /usr/local/tomcat/webapps
