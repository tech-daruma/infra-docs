# Troubleshooting tips


## Deleting a namespace that is stuck at deletion
```shell
kubectl get namespace "$PROJECT" -o json | jq 'del(.spec.finalizers[] | select("kubernetes"))' | curl -s -k -H "Content-Type: application/json" -X PUT -o /dev/null --data-binary @- http://localhost:8001/api/v1/namespaces/$PROJECT/finalize && echo "Killed namespace: $PROJECT"
```