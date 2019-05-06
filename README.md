# cbyg-jenkins
Jenkins helm chart

### How to package and add Jenkins Chart to repo
```
$ cd Projects/phono-helm
$ helm package ../cbyg-jenkins/charts/jenkins/
Successfully packaged chart and saved it to: /home/gmarcote/Projects/phono-helm/jenkins-0.1.0.tgz
$ helm repo index . # create or update the index.yaml for repo
$ git add .
$ git commit -m 'Project Jenkins chart version 0.1.0'
$ git push
```

Add and update repo:
```
$ helm repo add phono-helm https://github-oauth@raw.githubusercontent.com/gonzalomarcote/phono-helm/master/
$ helm repo update
$ helm search jenkins
```

Install example:
```
$ helm install --dry-run --debug --name jenkins --namespace jenkins phono-helm/jenkins
$ helm install --name jenkins --namespace jenkins phono-helm/jenkins

```
