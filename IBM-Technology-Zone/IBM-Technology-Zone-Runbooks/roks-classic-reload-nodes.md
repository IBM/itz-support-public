# Reload Worker Nodes on Classic ROKS Clusters

You can reload the workers with the following commands

`ibmcloud oc worker ls -c <cluster_name_or_ID>`  
`ibmcloud oc worker reload -c <cluster_name_or_ID> -w <workerID_1>`  

you can then validate the change with the following commands  

`oc debug node/<node_name in OCP>`  
`$ chroot /host`  
`# cat /.docker/config.json`  

### Support  

For any questions, contact ITZ support - techzone.help@ibm.com  
