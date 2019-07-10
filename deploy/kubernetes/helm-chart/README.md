Steps for sock shop demo install

```
helm install stable/nginx-ingress

helm install .
```

If you need customize your ingress rules you can use the following:
```
cat <<EOF >ingress.yaml
apiVersion: extensions/v1beta1
kind: Ingress
metadata:
  name: sockshop
spec:
  backend:
    serviceName: front-end
    servicePort: 80
EOF

kubectl apply -f ingress.yaml
```
