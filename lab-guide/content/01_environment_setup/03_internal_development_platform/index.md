## Internal Development Platform Setup

When the codespaces instance is fully initialized and running, you'll be able to access the IDP components.

### Login to ArgoCD

Get ArgoCD password:

```
ARGOCDPWD=$(kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d)
echo $ARGOCDPWD
```

The username is: `admin`

Change to `Ports` tab and open ArgoCD (port `30100`) & log in as `admin`.

![ArgoCD Login](../../../assets/images/01_03_argocd.png)

![ArgoCD Overview](../../../assets/images/01_03_argocd_overview.png)

### Login to Backstage

Backstage is available (port `30105`) without any login credentials.

Change to `Ports` tab and open Backstage (port `30105`).

![Backstage Login](../../../assets/images/01_03_backstage.png)