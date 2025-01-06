## GitHub Repository Setup

You will need a GitHub account.

The source repository for this lab is: 

https://github.com/dynatrace-wwse/enablement-openpipeline-segments-iam

The reference repository (*not* used for this lab) is:

https://github.com/dynatrace-perfclinics/platform-engineering-demo 

### Fork Repository

Create your own fork of the source repository.

![Create Fork](../../../assets/images/01_02_github_create_fork.png)

*note* running this lab will modify the repository, you will need to delete your fork and start from the beginning (new fork) every time you run this lab!

### ⚠️ Enable Actions in your Fork ⚠️

> ⚠️ This step is important! ⚠️

This lab uses one GitHub action to automatically merge Pull Requests when apps are onboarded.

In your fork, go to `Actions` and click the green button: `I understand my workflows, go ahead and enable them`.

![GitHub Actions](../../../assets/images/01_02_github_enable_actions.png)

### Delete ArgoCD Hook Jobs (optional)

If you do not have an OAuth Client, you will not be able to execute ArgoCD Hook Jobs that generate BizEvent data.

![ArgoCD Hook Jobs](../../../assets/images/01_02_argohookjobs.png)

In your fork, go to `Code`.  Navigate to `/apptemplates/simplenodeservice-content/argohookjobs.yml`.

Edit the file, delete all contents, and replace with `---`.  Save the file.

### Create Codespaces Instance

In your fork:

1. Switch to the `main` branch
1. Click the green `Code` button
1. Change to `Codespaces`
1. Click the `...` and choose `New with options...`

![New Codespaces Instance](../../../assets/images/01_02_codespaces_new_with_options.png)

**Warning!** Do not click the green "Create codespace on codespace" button!!

Fill in the form and launch the codespace.

![Codespaces Configuration](../../../assets/images/01_02_codespaces_machine_type.png)

![Codespaces Secrets](../../../assets/images/01_02_codespaces_new_secrets.png)

If you have **already** defined the environment variables in your repository, you'll see a screen asking you to associate those secrets with this repository. Please check the boxes as shown below.

![Codespaces Existing Secrets](../../../assets/images/01_02_codespaces_existing_secrets.png)

The codespaces instance will launch and the setup scripts will execute.

Wait until the `Running postStartCommand...` disappears. It should take ~10 minutes.

### Activate Kubernetes Experience in Dynatrace

When the codespaces instance is finished launching, go to the Terminal prompt and run the following command:

```text
kubectl get pods -n dynatrace
```

![Dynatrace ActiveGate Pod](../../../assets/images/01_02_dynatrace_activegate_pod.png)

Run this command every couple minutes until you see the `platform-engineering-demo-activegate-0` pod running and ready.

Navigate to the Dynatrace tenant and launch the `Kubernetes` App.  You should eventually see a cluster pending activation.  Activate the Kubernetes Experience for your `platform-engineering-demo` cluster.

![Dynatrace Kubernetes Experience Activation](../../../assets/images/01_02_kubernetes_experience.png)
