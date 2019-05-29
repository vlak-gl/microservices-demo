Steps for sock shop demo install

```
helm install .

helm install stable/nginx-ingress

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
