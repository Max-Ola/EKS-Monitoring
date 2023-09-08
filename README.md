# EKS-Monitoring
Setup Prometheus and Grafana for AWS EKS cluster monitoring using Pulumi and Helm


Explanation

This Pulumi program creates multiple resources and finally exports some constants we defined:

Creates a VPC
Creates the EKS Cluster.
Creates 2 namespaces, one for Prometheus and the other for Grafana.
Creates an Nginx deployment running on port 80 with a replica set of 2.
Creates a Load Balancer service for the Nginx deployment.
Use Helm to install Prometheus and Grafana in the Cluster.
Changed the default service type of Prometheus and Grafana services from ClusterIP to LoadBalancer to access them from the browser.
Outputs the Grafana service URL, Prometheus service URL(external), Prometheus service URL(local), EKS Cluster name, the cluster kube config, and the Nginx service endpoint.
Deploy application
Next, run the Pulumi up command to deploy the project. This would take some time. After everything is completed, you should get an output similar to this:

