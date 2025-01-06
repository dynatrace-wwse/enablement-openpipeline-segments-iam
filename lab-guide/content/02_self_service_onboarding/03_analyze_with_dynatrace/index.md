## Analyze with Dynatrace

Explore the observability data captured by Dynatrace for the new applications

### Explore Kubernetes App

Let's quickly validate that Dynatrace is properly monitoring our Platform Kubernetes Cluster. For this we open the Kubernetes App.

Lets validate that we have no issues across all layers of Kubernetes (cluster, namespaces, workloads ...).

We can also explore the ready-made dashboards to get more insights into e.g: Cluster health

![Kubernets App](../../../assets/images/02_03_kubernetes_app.png)

Use the Kubernetes App to locate the new applications.  Each application is deployed into its own namespace.  Check the status of the different components deployed into the namespace.

### Explore IDP SimpleNodeServices Dashboard

If you haven't already, import the [IDP SimpleNodeServices](todo/dashboard) Dashboard into the Dynatrace environment.

![IDP SimpleNodeServices Dashboard](../../../assets/images/02_03_idp_simplenodeservices_dashboard.png)

Use the dashboard to observe the health of the SimpleNodeService applications/services deployed on the IDP.

Change the variable selectors for `Namespace` to find the relevant details for the (4) application namespaces.

