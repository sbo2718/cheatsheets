# Kubernetes and kubectl

## Weblinks

[Official cheatsheet](https://kubernetes.io/de/docs/reference/kubectl/cheatsheet/)

[Probes](https://kubernetes.io/docs/tasks/configure-pod-container/configure-liveness-readiness-startup-probes/#define-a-liveness-http-request)

[Good guide on the dashboard](https://www.replex.io/blog/how-to-install-access-and-add-heapster-metrics-to-the-kubernetes-dashboard)

## Commands

Get the exposed port of 'my-service':
`export NODE_PORT=$(kubectl get services/my-service -o go-template='{{(index .spec.ports 0).nodePort}}')`

get pods running a deployment based on labels:
`export POD_NAME=$(kubectl get pods -l app=my-app  -o go-template --template '{{range .items}}{{.metadata.name}}{{"\n"}}{{end}}')
`