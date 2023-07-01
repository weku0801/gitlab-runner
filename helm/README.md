```
helm repo add gitlab https://charts.gitlab.io
helm repo update gitlab
```

```
export GITLAB_NS=
```

```
export GITLAB_CI_URL=
```

```
export GITLAB_CI_TOKEN=
```

```
helm install --create-namespace -n $GITLAB_NS gitlab-runner --set gitlabUrl=$GITLAB_CI_URL,runnerRegistrationToken=$GITLAB_CI_TOKEN -f ./values.yaml gitlab/gitlab-runner
```

```
# helm upgrade -n gitlab-smartx-com gitlab-runner --set gitlabUrl=$GITLAB_CI_URL,runnerRegistrationToken=$GITLAB_CI_TOKEN -f ./values.yaml gitlab/gitlab-runner
```