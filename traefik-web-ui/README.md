<h2>Description</h2>
<p>Traefik web ui</p>
<h2>Install</h2>
<p><b>kubectl apply -f https://raw.githubusercontent.com/ciseldevops/k8s/master/traefik-web-ui/values.yaml</b></p>

<h2>Upgrade</h2>
<p>Modifier le fichier yaml : le tag du repository correspond à la version. Il peut être changé pour atteindre une nouvelle version </br>
</p>
<p><b>
 kubectl rolling-update NAME -f https://raw.githubusercontent.com/ciseldevops/k8s/master/traefik-web-ui/values.yaml </b> </br>
</p>

<h2>Clean</h2>
<p>kubectl delete -f https://raw.githubusercontent.com/ciseldevops/k8s/master/traefik-web-ui/values.yaml</p>
<h2>Test et accès</h2>
<p>En interne : <b>traefikuik8sdev.cisel.lan</b></p>

<h2>Autres infos</h2>
<p>Empty</p>
