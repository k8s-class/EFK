# EFK
```
1. helm repo add akomljen-charts \
    https://raw.githubusercontent.com/komljen/helm-charts/master/charts/

2. helm install --name es-operator \
    --namespace logging \
    akomljen-charts/elasticsearch-operator

3. kubectl get pods -n logging

4. kubectl get CustomResourceDefinition

5. helm install --name efk \
    --namespace logging \
    akomljen-charts/efk

6. kubectl get pods -n logging

7. kubectl get cronjob -n logging


8. kubectl port-forward efk-kibana-6cf88598b6-xlkv2 5601 -n logging


9. Then, go to Discover menu item, configure the index to kubernetes_cluster*, choose a @timestamp and Kibana is ready. You should see all the logs from all namespaces in your Kubernetes cluster.

```
