# pgodemo

# Useful Links
JMeter:  https://jmeter.apache.org/download_jmeter.cgi
Crunchy Operator 5.0 Preview Doc:  https://pgo5-docs-preview.crunchydata.com/quickstart/

# Install ArgoCD
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
kubectl patch svc argocd-server -n argocd -p '{"spec": {"type": "LoadBalancer"}}'
oc get secret -n argocd argocd-initial-admin-secret  --template={{.data.password}} | base64 -d
