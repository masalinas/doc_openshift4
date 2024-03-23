# Description
Install Openshift 4 with crc

# Download the crc

**STEP01**: Download crc client from [Redhat Openshift Local](https://console.redhat.com/openshift/create/local)

**STEP02**: Download pull-secret.txt file from the same link


[pull-secret.txt](https://github.com/masalinas/doc_openshift4/files/14732976/pull-secret.txt)

**STEP03**: execute configuration

```
crc config set pull-secret-file ./pull-secret.txt
```

STEP04: start installation

```
crc start

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
