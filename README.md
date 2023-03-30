# Personal helm charts

## Add repo
- To add repo:
    ```
    helm repo add yc-courses-ru-devsecops-helm-charts https://yandex-cloud-examples.github.io/yc-courses-ru-devsecops-helm-charts/
    ```
- Update repos
  ```
  helm repo update
  ```
- To check charts in added repo:
    ```
    helm search repo yc-courses-ru-devsecops-helm-charts
    ```


## Add chart to repo
- Generate helm package from chart folder
  ```
  helm package .
  ```
- Copy generated `<chart_name>.tgz` to this repository dir
- Update index.yaml file on root of repository dir
  ```
  helm repo index .  --url "https://yandex-cloud-examples.github.io/yc-courses-ru-devsecops-helm-charts/"
  ```
- Commit changes



## Current charts
```
❯ helm search repo yc-courses-ru-devsecops-helm-charts
NAME                            CHART VERSION   APP VERSION     DESCRIPTION
yc-courses-ru-devsecops-helm-charts/defectdojo   1.6.45          2.16.1          A Helm chart for Kubernetes to install DefectDojo
```
