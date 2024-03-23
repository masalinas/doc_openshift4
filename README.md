# Description
Install Openshift 4 with crc

## Installation STEPS

**STEP01**: download crc CLI

Download crc client from [Redhat Openshift Local](https://console.redhat.com/openshift/create/local)

**STEP02**: download pull secret for the installation

Download pull-secret.txt file from the same link

[pull-secret.txt](https://github.com/masalinas/doc_openshift4/files/14732976/pull-secret.txt)

**STEP03**: execute configuration

Configure pull secret before start installation

```
$ crc config set pull-secret-file ./pull-secret.txt
```

**STEP04**: start cluster installation

```
$ crc start

...
...
INFO Operators are stable (3/3)...                
INFO Adding crc-admin and crc-developer contexts to kubeconfig... 
Started the OpenShift cluster.

The server is accessible via web console at:
  https://console-openshift-console.apps-crc.testing

Log in as administrator:
  Username: kubeadmin
  Password: yx9Rq-X4Mrd-XZLkU-UeyAI

Log in as user:
  Username: developer
  Password: developer

Use the 'oc' command line interface:
  $ eval $(crc oc-env)
  $ oc login -u developer https://api.crc.testing:6443
```

**STEP05**: check cluster status

```
$ crc status
CRC VM:          Running
OpenShift:       Running (v4.14.12)
RAM Usage:       6.261GB of 9.353GB
Disk Usage:      20.71GB of 32.68GB (Inside the CRC VM)
Cache Usage:     38.18GB
Cache Directory: /Users/miguel/.crc/cache
```

**STEP06**: access openshift console

```
$ crc console
```

![Captura de pantalla 2024-03-23 a las 17 57 37](https://github.com/masalinas/doc_openshift4/assets/1216181/e313e583-b67e-4ca5-8960-ed10d936c24a)

**STEP07**: stops the OpenShift cluster

```
$ crc stop 
```

**STEP08**: completely deletes the cluster

```
$ crc delete 
```

## Some links

- [IBM Openshift Local] (https://developer.ibm.com/blogs/install-openshift-4-on-your-laptop/)


