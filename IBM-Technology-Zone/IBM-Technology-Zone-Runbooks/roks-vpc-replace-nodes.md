# Replace(Reload) Worker Nodes on ROKS  VPC Gen2 Clusters

VPC cluster worker nodes cannot be reloaded.  
Instead, delete the worker node and then rebalance the worker pool by using the 'worker replace' operation.  

`ibmcloud oc worker ls -c <cluster_name_or_ID>`  
`ibmcloud oc worker replace --cluster <cluster_name_or_ID> --worker <worker_node_ID>`  

`oc debug node/<node_name in OCP>`  
`$ chroot /host`  
`# cat /.docker/config.json`  

### Support  

For any questions, contact ITZ support - techzone.help@ibm.com  
