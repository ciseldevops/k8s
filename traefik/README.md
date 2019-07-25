<h2>Description</h2>
<p>Traefik as an Ingress controller for a Kubernetes cluster</p>
<h2>Install</h2>
<p><b>kubectl apply -f https://raw.githubusercontent.com/ciseldevops/k8s/master/traefik/values.yaml</b></p>

<h2>Upgrade</h2>
<p>Modifier le fichier yaml : le tag du repository correspond à la version. Il peut être changé pour atteindre une nouvelle version </br>
</p>
<p><b>
 kubectl rolling-update NAME -f https://raw.githubusercontent.com/ciseldevops/k8s/master/traefik/values.yaml </b> </br>
  Le ReleaseLocalName correpond au nom de la realease en faisant par ex. helm list
</p>

<h2>Clean</h2>
<p>kubectl delete -f https://raw.githubusercontent.com/ciseldevops/k8s/master/traefik/values.yaml</p>
<h2>Test et accès</h2>
<p>En interne : <b>node:port</b></p>

<h2>Autres infos</h2>
<p>Empty</p>
