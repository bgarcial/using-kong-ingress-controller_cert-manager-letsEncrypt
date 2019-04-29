### TLS encryption with Kong, kong-ingress-controller, cert-manager and LetsEncrypt

- Service Image: Hashicorp Echo tiny HTTP server - 
    - https://github.com/hashicorp/http-echo
    - https://hub.docker.com/r/hashicorp/http-echo/

- Kong Ingress controller 0.3.0
- Kong 0.1.0
- cert-manager v0.7.0  
```
helm install \
      --name cert-manager \
      --namespace cert-manager \
      --version v0.7.0 \
      jetstack/cert-manager

```

- Acme Kong Kube Helper - https://github.com/ollystephens/acme-kong-kube-helper 

We are using acme kong kube helper like a third container inside the Kong Ingress controller deployment