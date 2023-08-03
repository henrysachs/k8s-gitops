# Hachs Cluster Setup 

Talos
    Grub
    custom patch files
Cilium 
    Hubble
    LB IPAM
    Servicemesh
    Ingress
    Quotas 
Age
Flux


## Age Key Encryption

Get the Age key from one of the maintainers and do the following (assuming the key is in the secrets folder)

```bash
mkdir -p ~/.config/sops/age
cp secrets/age-key.txt ~/.config/sops/age/keys.txt
```


