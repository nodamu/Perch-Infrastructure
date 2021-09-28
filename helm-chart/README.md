# Perch-Infrastructure
- Repository for Perch IaC, GitOps and Helm Charts
  
## Running Perch on a local kubernetes cluster
- First install the bitnami mongodb helm chart
 ```bash 
  helm install mongodb --set auth.rootPassword=root,auth.username=admin,auth.password=perch,auth.database=perch,architecture=replicaset bitnami/mongodb
```

- Then install the perch api chart
```bash
 helm install -f values-dev perch-api .
```

