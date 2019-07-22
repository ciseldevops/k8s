<h2>Commande d'installation</h2>
<p>helm install </p>

<p>
  helm install stable/grafana \
--name grafana \
--namespace ntnx-system \
--set persistence.enabled=true \
--set datasources."datasources\.yaml".apiVersion=1 \
--set datasources."datasources\.yaml".datasources[0].name=Prometheus \
--set datasources."datasources\.yaml".datasources[0].type=prometheus \
--set datasources."datasources\.yaml".datasources[0].url=http://prometheus-k8s.ntnx-system.svc.cluster.local:9090 \
--set datasources."datasources\.yaml".datasources[0].access=proxy \
--set datasources."datasources\.yaml".datasources[0].isDefault=true \
--set dashboards.default.kube-capacity.gnetId=5309 \
--set dashboards.default.kube-capacity.revision=1 \
--set dashboards.default.kube-capacity.datasource=Prometheus \
--set dashboards.default.kube-cluster-health.gnetId=5312 \
--set dashboards.default.kube-cluster-health.revision=1 \
--set dashboards.default.kube-cluster-health.datasource=Prometheus \
--set dashboards.default.kube-cluster-status.gnetId=5315 \
--set dashboards.default.kube-cluster-status.revision=1 \
--set dashboards.default.kube-cluster-status.datasource=Prometheus \
--set dashboards.default.kube-deployment.gnetId=5303 \
--set dashboards.default.kube-deployment.revision=1 \
--set dashboards.default.kube-deployment.datasource=Prometheus \
--set dashboards.default.kube-master-status.gnetId=5318 \
--set dashboards.default.kube-master-status.revision=1 \
--set dashboards.default.kube-master-status.datasource=Prometheus \
--set dashboards.default.kube-nodes.gnetId=5324 \
--set dashboards.default.kube-nodes.revision=1 \
--set dashboards.default.kube-nodes.datasource=Prometheus \
--set dashboards.default.kube-pods.gnetId=5327 \
--set dashboards.default.kube-pods.revision=1 \
--set dashboards.default.kube-pods.datasource=Prometheus \
--set dashboards.default.kube-resource-request.gnetId=5321 \
--set dashboards.default.kube-resource-request.revision=1 \
--set dashboards.default.kube-resource-request.datasource=Prometheus \
--set dashboards.default.kube-statefulset.gnetId=5330 \
--set dashboards.default.kube-statefulset.revision=1 \
--set dashboards.default.kube-statefulset.datasource=Prometheus \
--set dashboardProviders."dashboardproviders\.yaml".apiVersion=1 \
--set dashboardProviders."dashboardproviders\.yaml".providers[0].orgId=1 \
--set dashboardProviders."dashboardproviders\.yaml".providers[0].type=file \
--set dashboardProviders."dashboardproviders\.yaml".providers[0].disableDeletion=false \
--set dashboardProviders."dashboardproviders\.yaml".providers[0].options.path="/var/lib/grafana/dashboards/default" \
--set service.type=NodePort
</p>

<h2>Procédure de maj</h2>
<p>Modifier le fichier yaml : le tag du repository correspond à la version. Il peut être changé pour atteindre une nouvelle version</p>
<p>Une fois le fichier modifié, les commandes suivantes sont utilisées pour mettre à jour le pod :<br/>
  kubectl delete -f https://github.com/ciseldevops/k8s/edit/master/Sample/sample.yaml <br/>
  kubectl create -f https://github.com/ciseldevops/k8s/edit/master/Sample/sample.yaml
</p>

<h2>Test et accès</h2>
<p>En interne : <b>http://grafanak8sdev.cisel.lan</b></p>

<h2>Autres infos</h2>
<p>Empty</p>
