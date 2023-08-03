# Flux Bootstrap

created an accesstoken that you can find in the yaml file 
ran:

```bash
flux bootstrap gitlab --owner=hachs-homelab --repository=setup --branch=main --path=kubernetes/apps --deploy-token-auth
```

this creates a deploy token in the repository so the authentication doesn't happen with you credentials

next we use the sops key from this repo and add it to flux so it can decrypt secrets in our cluster

```bash
cd secrets
kubectl -n flux-system create secret generic sops-age --from-file=age.agekey=age-key.txt
```
