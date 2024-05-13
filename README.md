
Install openshift virt operator and deploy a HyperConverged instance.


create a file env.sh and populate with keys from Docker

```
export CLIENT_ID=xxxx
export CLIENT_SECRET=xxxx
export PULL_SECRET=xxxx
```

run: `source env.sh`


run `helm install --set clientId=$CLIENT_ID --set clientSecret=$CLIENT_SECRET --set pullSecret=$PULL_SECRET testcontainers-cloud ./helm/`

To uninstall run `helm uninstall testcontainers-cloud`