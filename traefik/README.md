<h2>Description</h2>
<p>Traefik as an Ingress controller for a Kubernetes cluster</p>
<h2>Install</h2>
<p><b>git clone https://github.com/ciseldevops/k8s.git </br>
  cd k8s/grafana </br>
  helm install stable/grafana --values=values.yaml</b></p>


<h2>Upgrade</h2>
<p>Modifier le fichier yaml : le tag du repository correspond à la version. Il peut être changé pour atteindre une nouvelle version </br>
</p>
<p>Une fois le fichier modifié, les commandes suivantes sont utilisées pour la maj : <br/>
  <b>git clone https://github.com/ciseldevops/k8s.git </br>
  cd k8s/grafana </br>
  helm upgrade ReleaseLocalName stable/grafana --values=values.yaml </b> </br>
  Le ReleaseLocalName correpond au nom de la realease en faisant par ex. helm list
</p>

<h2>Clean</h2>
<p>helm delete -f ... --purge</p>
<h2>Test et accès</h2>
<p>En interne : <b>http://grafanak8sdev.cisel.lan</b></p>

<h2>Autres infos</h2>
<p>Empty</p>
