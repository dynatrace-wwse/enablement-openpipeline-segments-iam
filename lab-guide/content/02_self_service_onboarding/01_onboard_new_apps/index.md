## Onboard New Apps

Use Backstage to create (4) new applications on the internal development platform (IDP).

### Create New Component

Navigate to Backstage (using port 30105 of your codespaces instance).  

![Backstage Create](../../../assets/images/02_01_backstage_create.png)

Click on `Create` near the top right corner of the page.

From the Templates, locate `Create a New Application` and click on `Choose`.

![Create a New Application](../../../assets/images/02_01_create_new_application.png)

Follow the 4 step template to create a new application using these values:

| Field                   | Value                       |
|-------------------------|-----------------------------|
| Project Name            | SimpleNodeService           |
| Team Identifier         | team01                      |
| Team Full Name          | Team 01                     |
| Team Email              | team01@dynatrace.training   |
| App Version             | 1.0.2                       |
| Release Stage           | qa                          |
| DORA Enabled            | enabled                     |
| Include Security Scans  | enabled                     |
| Include DT Config       | enabled                     |

![Review and Create](../../../assets/images/02_01_review_and_create.png)

Review the new application details and click `Create`.

### Create Additional Components

Repeat the previous steps, 3 more times, to onboard a total of (4) applications.  Use the following values:

| Field                   | Value                       | Value 2                    | Value 3                    | Value 4                    |
|-------------------------|-----------------------------|----------------------------|----------------------------|----------------------------|
| Project Name            | SimpleNodeService           | SimpleNodeService          | SimpleNodeService          | SimpleNodeService          |
| Team Identifier         | team01                      | team01                     | team02                     | team02                     |
| Team Full Name          | Team 01                     | Team 01                    | Team 02                    | Team 02                    |
| Team Email              | team01@dynatrace.training   | team01@dynatrace.training  | team02@dynatrace.training  | team02@dynatrace.training  |
| App Version             | 1.0.2                       | 1.0.2                      | 1.0.2                      | 1.0.2                      |
| Release Stage           | qa                          | staging                    | qa                         | staging                    |
| DORA Enabled            | enabled                     | enabled                    | enabled                    | enabled                    |
| Include Security Scans  | enabled                     | enabled                    | enabled                    | enabled                    |
| Include DT Config       | enabled                     | enabled                    | enabled                    | enabled                    |

### Review New Components

![All Components](../../../assets/images/02_01_all_components.png)

In your Backstage catalog, you should now have (4) components for the (4) new applications.

### Validate App Deployment

Navigate to the ArgoCD instance (using port 30100 of your codespaces instance).

![ArgoCD Apps](../../../assets/images/02_01_argocd_apps_deployed.png)

ArgoCD will automatically deploy the new applications based on the manifests created in the Git repository by Backstage.

ArgoCD will reconcile the configurations every 3 minutes.  When a change is detected, it will automatically sync and deploy the changes to the Kubernetes cluster.  This process may take 5-10 minutes total for all (4) applications to be deployed successfully.

Wait for the apps to be deployed and for all (4) apps to show as `Healthy` and `Synced`.  In case of any issues with the sync, sync the app manually to try again.