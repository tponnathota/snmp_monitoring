# snmp_monitoring
SNMP Monitoring


Deploy Prometheus
1. kubectl create namespace prometheus
2. kubectl apply -f prometheus-config.yaml -n prometheus
3. kubectl apply -f prometheus-deployment.yaml -n prometheus
4. kubectl apply -f prometheus-service.yaml -n prometheus
5. kubectl get service prometheus-service -n prometheus --- get external ip of prometheus instance

Deploy Grafna
1. kubectl create namespace grafana
2. kubectl apply -f grafana.yaml --namespace=grafana

Validate Grafana deployemnt
1. kubectl get pvc --namespace=grafana -o wide
2. kubectl get deployments --namespace=grafana -o wide
3. kubectl get svc --namespace=grafana -o wide
4. kubectl get all --namespace=grafana
5. kubectl port-forward service/grafana 3000:3000 --namespace=grafana  (If needed)






