# ELK_helm_4_vCluster
Logstash , Elasticsearch and Kibana helm charts to deploy ELK for a Kind cluster.





helm repo add ELK_4_vCluster https://kirillyesikov.github.io/ELK_helm_4_vCluster/ 


helm upgrade --install elastic ELK_4_vCluster/elasticsearch  -n logging --create-namespace --set replicas=1

helm upgrade --install kibana ELK_4_vCluster/kibana  -n logging  --set replicas=1

helm upgrade --install logstash ELK_4_vCluster/logstash  -n logging --set replicas=1

