# Материалы для курса «DevSecOps в облачном CI/CD»

https://practicum.yandex.ru/profile/ycloud-devsecops/subscribe


## Персональные Helm-чарты

### Добавление репозитория

- Добавьте репозиторий:
    ```
    helm repo add yc-courses-ru-devsecops-helm-charts https://yandex-cloud-examples.github.io/yc-courses-ru-devsecops-helm-charts/
    ```
- Обновите репозиторий:
  ```
  helm repo update
  ```
- Проверьте репозиторий на наличие чартов:
    ```
    helm search repo yc-courses-ru-devsecops-helm-charts
    ```


### Добавление чарта в репозиторий

- Создайте пакет Helm из папки чарта:
  ```
  helm package .
  ```
- Скопируйте созданный `<chart_name>.tgz` в директорию репозитория.
- Обновите файл `index.yaml` в корневой директории репозитория.
  ```
  helm repo index .  --url "https://yandex-cloud-examples.github.io/yc-courses-ru-devsecops-helm-charts/"
  ```
- Нажмите **Commit changes**.


### Текущие чарты

```
❯ helm search repo yc-courses-ru-devsecops-helm-charts
NAME                            CHART VERSION   APP VERSION     DESCRIPTION
yc-courses-ru-devsecops-helm-charts/defectdojo   1.6.45          2.16.1          A Helm chart for Kubernetes to install DefectDojo
```
