# IBM Cloud ROKS/Kubernetes Command Line Login Context

This run book describes how to get a command line login context for a ROKS or Kubernetes (IKS) cluster deployed in IBM Cloud.

## Pre-reqs

- IBM Cloud CLI (`ibmcloud`) installed with the `container-service` plugin installed.
  - **NOTE:** In this document, `ic` is an alias for `ibmcloud`.

- OCP CLI (`oc`) installed if you are working with a ROKS cluster.

- Kubernetes CLI (`kubectl`) installed if you are working with an IKS cluster.

## Steps

- Determine the IBM Cloud account where your ROKS or IKS cluster is deployed.

- Log into IBM Cloud command line.
```
$ ic login --sso
```
As part of the IBM Cloud login process, you will be prompted for the account you want to use as a list of numbered accounts.  Provide the number associated with the account where the target cluster is deployed.

- Establish the cluster login context:
```
$ ic ks cluster config -c CLUSTER_NAME_OR_ID --admin
```

At this point you can use the OCP CLI (`oc`) or Kubernetes CLI (`kubectl`) depending on what kind of target cluster you are logged into.

The login context is effective in all command shells that you have open or will open.

### Support

For any questions, contact ITZ support - techzone.help@ibm.com
