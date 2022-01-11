# Fix Error EOF on Fyre OCP Clusters  

1.  SSH to the Load Balancer VM  

2.  From the Load Balancer Run (Replace [node_name] with the actual name of each node)  

`ssh core@[node_name] `  
`sudo -i `  
`export KUBECONFIG=/etc/kubernetes/static-pod-resources/kube-apiserver-certs/secrets/node-kubeconfigs/lb-int.kubeconfig `  
`oc get csr -o name | xargs oc adm certificate approve `  

3. After a few minutes, try to access the web console, it should now be accessible  

### Support

For any questions, contact ITZ support - techzone.help@ibm.com
