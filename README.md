
Install openshift virt operator and deploy a HyperConverged instance.

create a file env.sh and populate with keys from Docker and a unique ZONE_NAME e.g. "my-test-tcc-zone"

```
export CLIENT_ID=xxxx
export CLIENT_SECRET=xxxx
export PULL_SECRET=xxxx
export ZONE_NAME=xxxx
```

run: `source env.sh`

run `helm install --set clientId=$CLIENT_ID --set clientSecret=$CLIENT_SECRET --set pullSecret=$PULL_SECRET --set zoneName=$ZONE_NAME testcontainers-cloud ./helm/`

run `echo "cloud.endpoint=https://eks-us.workloads.testcontainers.cloud/lease?zone=$CLIENT_ID-$ZONE_NAME" > ~/.config/testcontainers/cloud.properties`


To uninstall run `helm uninstall testcontainers-cloud`