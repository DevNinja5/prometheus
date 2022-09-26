## Deploy Application

```
kubectl apply -f application 
```

## Deploy prometheus operator

```
helm upgrade --install prometheus-operator prometheus --namespace prometheus-operator --create-namespace
```


## Deploy grafana 

```
helm upgrade --install grafana grafana -n grafana --create-namespace
```

## Deploy prometheus resources

```
kubectl apply -f prometheus-resources
```


# Add Datasources in grafana

Datasource name: Application
Application datasource : http://prometheus-operated.application:9090



Datasource name: Prometheus Nodes
Prometheus datasource : http://prometheus-operated.prometheus-operator:9090