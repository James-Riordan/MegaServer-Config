#Configure persistent volume for Tekton
kubectl create configmap config-artifact-pvc \
--from-literal=size=10Gi \
--from-literal=storageClassName=manual \
-o yaml -n tekton-pipelines \
--dry-run=true | kubectl replace -f -

# Installing kustomize (temporarily until we no longer use kustomize)

brew install kustomize

env

in argocd-task-cm.yml replace argocd_server with argo's url

# Applying triggers

kubectl apply --filename https://storage.googleapis.com/tekton-releases/triggers/latest/release.yaml
