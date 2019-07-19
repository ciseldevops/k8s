helm repo add mattermost https://helm.mattermost.com
helm install --name mattermost -f values.yaml mattermost/mattermost-team-edition
