# Notes

## Connect to the kubeconfig

```bash
export KUBECONFIG="/Users/christiankotait/veeton/scraping/k8s_crawlab/kubeconfig.yml"
```

Set an alias for the kubectl command

```bash
alias k="kubectl"
```

## MongoDB

To connect to the mongodb hosted on OVH using mongosh, use the following command:

```bash
mongosh "mongodb+srv://<USERNAME>:<PASSWORDD>@mongodb-05001237-od503bbcb.database.cloud.ovh.net/admin?replicaSet=replicaset&tls=true"
```

## Dashboard

To delete all the ressources related to the dashboard:

```bash
kubectl delete -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.7.0/aio/deploy/recommended.yaml
kubectl delete -f ovh_dashboard/dashboard-cluster-role-binding.yaml
```

## Tutorial and ressources used to spawn cluster

- For cert-bot: https://www.digitalocean.com/community/tutorials/how-to-set-up-an-nginx-ingress-with-cert-manager-on-digitalocean-kubernetes
- For the OVH Dashboard: https://help.ovhcloud.com/csm/en-gb-public-cloud-kubernetes-install-kubernetes-dashboard?id=kb_article_view&sysparm_article=KB0049828
