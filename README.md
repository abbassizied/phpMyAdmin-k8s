# phpMyAdmin-k8s

## steps to test concepts in killercude:

```sh
$ git clone https://github.com/abbassizied/phpMyAdmin-k8s.git
$ kubectl create namespace ams-database
$ kubectl config set-context --current --namespace=ams-database
$ kubectl apply -f ./phpMyAdmin-k8s
$ kubectl get svc
$ kubectl get pod mysql-article-sts-0 -o wide
$ kubectl get pod mysql-provider-sts-0 -o wide

# root-password: root
# user-username: user123
# user-password: pass123
# mysql-article-sts-0/3306
# mysql-provider-sts-0/3333

# List the pods
$ kubectl get pod -n ams-database
# Find the MySQL pod and copy its name by selecting it and pressing Ctrl+Shift+C
# Get a shell for the pod by executing the following command:
$ kubectl exec -it mysql-article-sts-0 -- /bin/bash
# OR kubectl exec -it pod mysql-article-sts-0 -- /bin/bash
# The pod shell replaces the main shell
# Type the following command to access the MySQL shell:
bash-5.1# mysql -u root
```
