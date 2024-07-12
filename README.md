# A modern and dark theme for ArgoCD

**Current Version: `0.1`v**

### Screenshots:

> ArgoCD UI

Applications Page

![argocd-applications](https://res.cloudinary.com/dor5uewzz/image/upload/v1720776187/readme-assets/argocd-applications_oefuwn.png)

Application Details

![argocd-application-details](https://res.cloudinary.com/dor5uewzz/image/upload/v1720776187/readme-assets/argocd-app-details_v3dhuu.png)

### Usage

1. `kubectl edit configmap -n argocd argocd-cm -o yaml`
2. Add `ui.cssurl` in `data` -> `ui.cssurl: https://cdn.jsdelivr.net/gh/code-crusher/argocd-gravity-theme@main/argo-theme.css` as below:
```YAML
data:
  admin.enabled: "true"
  application.instanceLabelKey: argocd.argoproj.io/instance
  exec.enabled: "false"
  server.rbac.log.enforce.enable: "false"
  statusbadge.enabled: "false"
  timeout.hard.reconciliation: 0s
  timeout.reconciliation: 180s
  ui.cssurl: https://cdn.jsdelivr.net/gh/code-crusher/argocd-gravity-theme@main/argo-theme.css
  url: https://argocd.example.com
```
3. Refersh the ArgoCD UI
