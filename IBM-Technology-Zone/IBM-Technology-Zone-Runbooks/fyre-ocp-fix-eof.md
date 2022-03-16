# Fix Error EOF on Fyre OCP Clusters  

1.  SSH to the Load Balancer VM  root / WinningWithTechZone2021!

2.  From the Load Balancer VM, run these commands 

`ssh core@[node_name]`      (Note: Replace [node_name] with the actual name of each node usually master0.CLUSTER_NAME.cp.fyre.ibm.com)  
`sudo -i `  
`export KUBECONFIG=/etc/kubernetes/static-pod-resources/kube-apiserver-certs/secrets/node-kubeconfigs/lb-int.kubeconfig `  
`oc get csr -o name | xargs oc adm certificate approve `  

3. After a few minutes, try to access the web console, it should now be accessible  

### Support

For any questions, contact ITZ support - techzone.help@ibm.com
