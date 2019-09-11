helm repo add mattermost https://helm.mattermost.com

helm install --name mattermost mattermost/mattermost-team-edition --values=https://raw.githubusercontent.com/ciseldevops/k8s/master/mattermost/values.yaml 
