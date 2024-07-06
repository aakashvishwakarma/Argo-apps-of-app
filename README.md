# Argo-apps-of-app

# Create an Application in ArgoCD UI ( Using either UI console or CLI)
    Here i m using UI and Edited it using below YML:
    # ArgoCD Application YML
    apiVersion: argoproj.io/v1alpha1
    kind: Application
    metadata:
    name: app-of-apps
    namespace: argocd

    spec:
    destination:
        namespace: argocd
        server: https://kubernetes.default.svc
    project: default
    source:
        path: apps
        repoURL: https://github.com/aakashvishwakarma/Argo-apps-of-app
        targetRevision: HEAD


