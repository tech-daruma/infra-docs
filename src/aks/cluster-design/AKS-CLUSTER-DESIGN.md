# AKS Cluster Design review and deployment process
  * Network design, placement, FW requirements

   ```sh 
   az aks show -g $RG -n $AKS --query networkProfile
   ```
  * Node Pool machine types, skus, app placement, labels, taints &   * rations, node pools for new breaking changes.
  * Monitoring evidence for VM SKU optimization to right size nodepools
  * RBAC – Kubernetes and 
  * Roles and responsibilities (IT infra, ITPE, EA, DevOps and Developers)
  * Troubleshooting 101
  * Upcoming updates from Microsoft and recommended actions. 