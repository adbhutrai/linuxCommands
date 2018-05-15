# Run following command to run minishift in Wimdows Virtual Box after downloading from 
# https://github.com/minishift/minishift/releases/latest and extracting in the C:\minishift directory.
# Then add this folder to PATH environment variable. Then use following command to set up VirtualBox as default driver
minishift config set vm-driver virtualbox
# Then run following command to run minishift
minishift start

# Sometimes it might not run so you have to use following command and then re-run 'minishift start' again
minishift delete --clear-cache

# You are logged in as:
oc login -u developer:admin

# To login as administrator:
   oc login -u system:admin