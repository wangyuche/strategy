# strategy


```
kubectl exec -c sleep \
    "$(kubectl get pod -l \
    app=sleep -o jsonpath='{.items[0].metadata.name}')" \
    -- curl -sS helloworld:5000/hello
```