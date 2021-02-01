# Open Match

## Run demo

```bash
kubectl apply --namespace open-match \
  -f https://open-match.dev/install/v1.1.0/yaml/01-open-match-core.yaml
```

```bash
kubectl apply --namespace open-match \
  -f https://open-match.dev/install/v1.1.0/yaml/06-open-match-override-configmap.yaml \
  -f https://open-match.dev/install/v1.1.0/yaml/07-open-match-default-evaluator.yaml
```

```bash
kubectl create namespace open-match-demo
kubectl apply --namespace open-match-demo \
  -f https://open-match.dev/install/v1.1.0/yaml/02-open-match-demo.yaml
kubectl port-forward --namespace open-match-demo service/om-demo 51507:51507
```
