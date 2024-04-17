# IBM Cloud ROKS/Kubernetes Command Line Login Context

This run book describes how to get a command line login context for a ROKS or Kubernetes (IKS) cluster deployed in IBM Cloud.

The process is described in the IBM Cloud documentation.

## Pre-reqs

- IBM Cloud CLI (`ibmcloud`) installed with the `container-service` plugin installed.
  - **NOTE:** In this document, `ic` is an alias for `ibmcloud`.

- OCP CLI (`oc`) installed if you are working with a ROKS cluster.

- Kubernetes CLI (`kubectl`) installed if you are working with an IKS cluster.

## Steps

See [Using an API key to log in to clusters](https://cloud.ibm.com/docs/openshift?topic=openshift-access_cluster#access_api_key)

- Determine the IBM Cloud account where your ROKS or IKS cluster is deployed.

- Log into IBM Cloud command line.
```
$ ic login --sso
```
As part of the IBM Cloud login process, you will be prompted for the account you want to use as a list of numbered accounts.  Provide the number associated with the account where the target cluster is deployed.

- (One time) If you do not already have an API Key for your user in the account you are using, create an API key for your user in the account, where the `<name>` is a name for the API key.
```
$ ic iam api-key-create <name>
```
The above command generates an API Key that you need to save in a safe place. *NOTE:* Once you have an API Key, it can be used indefinitely as long as it remains active.

- Now, logout of IBM Cloud and log back in using the API key.
```
$ ic logout
$ ic login --apikey API_KEY
```

- Get the cluster config for the cluster of interest.
```
$ ic oc cluster config -c CLUSTER_NAME
```

- Now, login to the ROKS cluster using `apikey` as the user name.
```
$ oc login -u apikey -p API_KEY
```

- At this point you should be able to run `oc` commands for for the cluster.

The IBM Cloud documentation describes some additional steps to get an OCP access token to the cluster. Those did not seem to be necessary.

