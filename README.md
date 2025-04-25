# GKE Ingress App Setup with SSL

This repository contains manifests to deploy:
- NGINX frontend
- Two backend services (httpbin, echo-server)
- GCE Ingress with managed SSL
- TLS secret for GKE compatibility

## Steps

1. Replace `your-domain.com` in `managed-cert.yaml` and `ingress.yaml`
2. Replace `my-ingress-ip` with your reserved IP name
3. Apply manifests:
   ```bash
   kubectl apply -f manifests/
   bash manifests/dummy-tls-secret.sh
   ```
4. Wait for the Ingress to be provisioned