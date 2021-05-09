# Metrics Case:

We have an api which has three endpoint shown at below;
* `/action` returning dummy 200 responses
* `/error_endpoint` returning 500 responses
* `/metrics` returning JSON metrics to enduser

This application running over 5000 port without any thirdparty dependencies
Api docker image is under => `https://hub.docker.com/r/kloiadocker/service_api`

### First;

* In this case develop a prometheus exporter which language you prefer and deploy those expoter and application into Kubernetes cluster (helm or direct k8s manifests)

### Second ;

* Deploy prometheus,grafana into kubernetes cluster after that connect metric-exporter to prometheus.
* Create alerts when 500 counts are increased in this application
* Confiure the HPA to scale the application based on `request_count` metrics (you can define your own threshold values)

Notice: Define password authentication to  Prometheus and Alertmanager applications

Good Luck !
If you have any question please call us 