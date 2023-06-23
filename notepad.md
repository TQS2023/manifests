kubectl create -f https://download.elastic.co/downloads/eck/2.8.0/crds.yaml

kubectl apply -f https://download.elastic.co/downloads/eck/2.8.0/operator.yaml

helm install mysql oci://registry-1.docker.io/bitnamicharts/mysql -n mysql --set global.storageClass="standard"

helm install ngrok-ingress-controller ngrok/kubernetes-ingress-controller
--namespace ngrok \
--create-namespace \
--set credentials.apiKey=---- \
--set credentials.authtoken=----