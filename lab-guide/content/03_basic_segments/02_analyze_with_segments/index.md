## Analyze with Segments

Analyze the applications in Dynatrace, this time using the newly created Segments.

### Explore IDP SimpleNodeServices Dashboard

If you haven't already, import the [IDP SimpleNodeServices](todo/dashboard) Dashboard into the Dynatrace environment.

![IDP SimpleNodeServices Dashboard](../../../assets/images/02_03_idp_simplenodeservices_dashboard.png)

Use the variable selector for `Namespace`.  Notice the long list of namespaces available to choose from.

![Namespace Selector](../../../assets/images/03_02_dashboard_namespace_selector.png)

The variable is configured (via DQL query) to pick from every Kubernetes namespace detected in the Dynatrace environment, across all clusters.

Apply Segment filters to the dashboard.  Click on the `Segments` icon to open the Segments filter prompt (next to the timeframe selector).

![Apply Segments](../../../assets/images/03_02_apply_segments_dashboard.png)

Start by applying the `idp-k8s-cluster` Segment filter and choose the `platform-engineering-demo` Kubernetes cluster.

Then apply the `idp-k8s-namespace` Segment filter and choose all (4) Kubernetes namespaces.

Click `Apply` to apply the Segment filter(s) to the dashboard.

Use the variable selector for `Namespace`.  Notice the reduced list of namespaces available to choose from.

