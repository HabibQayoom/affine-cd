# Affine-CD

## Overview
Affine-CD is a continuous deployment setup for the Affine project. This repository contains the configurations and scripts required for seamless deployment.

## Features
- Automated CD with Argocd
- Docker and Kubernetes support
 ## Manual Installation
1. Clone the repository in the Aks:
   ```bash
   git clone https://github.com/HabibQayoom/affine-cd.git
2. Create Namepace:
   ```bash
   kubetcl create namespace affine
3. Apply all Manifest files:
   ```bash
   kubectl apply -f .
4. For testing deploy :
   ```bash
    kubectl port-forward svc/affine 8080:80
  http://yourip:8080
 Or change the service type ClusterIp to NodePort 
 So they give a port 
  ```bash
  kubectl get svc -n affine
http://<yourip>:yournodeport
