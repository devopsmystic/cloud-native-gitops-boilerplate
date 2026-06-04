# Liferay Cloud Native GitOps Boilerplate
cd /home/me/Downloads/aws-srs-sandbox/cne-bootstrap/4jun

cp ~/dev/projects/cloud-native-gitops-boilerplate/liferay/projects/indus/config.json .

aws sso login

bash <(curl -sL https://raw.githubusercontent.com/liferay/liferay-portal/refs/heads/master/cloud/scripts/bootstrap.sh)

kubectl port-forward service/argocd-server 8080:443 \
   --namespace argocd-system