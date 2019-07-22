<h1>Sample devops Cisel deploy</h1>

<h2>Commande d'installation</h2>
<p>kubectl create -f https://github.com/ciseldevops/k8s/edit/master/Sample/sample.yaml </p>

<h2>Procédure de maj</h2>
<p>Modifier le fichier yaml : le tag du repository correspond à la version. Il peut être changé pour atteindre une nouvelle version</p>
<p>Une fois le fichier modifié, les commandes suivantes sont utilisées pour mettre à jour le pod :<br/>
  <b>kubectl delete -f https://github.com/ciseldevops/k8s/edit/master/Sample/sample.yaml</b>
  <b>kubectl create -f https://github.com/ciseldevops/k8s/edit/master/Sample/sample.yaml</b>
</p>

<h2>Test et accès</h2>
<p>En interne : <b>http://grafanak8sdev.cisel.lan</b></p>

<h2>Autres infos</h2>
<p>Empty</p>
