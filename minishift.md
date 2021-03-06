To setup minishift on windows using gitbash directory

Create environment variable MINISHIFT_HOME with directory of your minishift.
Add this environment varibale to Users Path variable as below:

Path = %Path%;%MINISHIFT_HOME%\;

> Run following command to run minishift in Windows Virtual Box after downloading from https://github.com/minishift/minishift/releases/latest and extracting in the C:\minishift directory.
> Then add this folder to PATH environment variable. Then use following command to set up VirtualBox as default driver
https://docs.openshift.org/latest/minishift/using/basic-usage.html

minishift profile set tutorial
minishift config set memory 8GB
minishift config set cpus 3
> minishift config set vm-driver virtualbox
minishift config set hyperv-virtual-switch "External (Wireless)"
minishift config set image-caching true
minishift addon enable admin-user
minishift addon enable anyuid
minishift config set openshift-version v3.11.0
minishift start --hyperv-virtual-switch


```
minishift config set vm-driver virtualbox
minishift config set cpus 2
minishift config set disk-size "40GB"
minishift config set memory "8GB"
minishift start --iso-url centos --show-libmachine-logs

```
> Then run following command to run minishift
minishift start

> Sometimes it might not run so you have to use following command and then re-run 'minishift start' again
minishift delete --clear-cache

> You are logged in as:
```
oc login -u developer:admin
```
> To login as administrator:
```
   oc login -u system:admin
```
Run command bellow to configure your shell to use oc client
```
 minishift 'oc-env'
```
https://github.com/OpenShiftDemos/openshift-cd-demo

https://access.redhat.com/documentation/en-us/red_hat_container_development_kit/3.4/html-single/getting_started_guide/index/index.html#persistent-configuration
