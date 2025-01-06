## Self-Service Onboarding

Using Backstage templates, deploy (4) new applications to the internal development platform (IDP).  Backstage will create new application manifests within the Git repository.  ArgoCD will automatically detect and deploy the new application manifests to the Kubernetes cluster.  Dynatrace will automatically observe the new applications.

* Onboard new applications using Backstage
* Explore the new applications deployed by ArgoCD
* Analyze the applications with Dynatrace
    - Analyze without Segments
