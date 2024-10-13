# Домашнее задание к занятию «Helm»

---

### Задание 1. Подготовить Helm-чарт для приложения

1. Необходимо упаковать приложение в чарт для деплоя в разные окружения. 
2. Каждый компонент приложения деплоится отдельным deployment’ом или statefulset’ом.
3. В переменных чарта измените образ приложения для изменения версии.

### Задание 2. Запустить две версии в разных неймспейсах

1. Подготовив чарт, необходимо его проверить. Запуститe несколько копий приложения.
2. Одну версию в namespace=app1, вторую версию в том же неймспейсе, третью версию в namespace=app2.
3. Продемонстрируйте результат.

---

### Ответ 1 


![Результат](https://github.com/loginochka/kuber/tree/main/media/2_5_deploy.png)


[Helm chart](https://github.com/loginochka/kuber/blob/main/h-10/nginx-chart/)

[Манифест deployment](https://github.com/loginochka/kuber/blob/main/h-10/nginx-chart/templates/deployment.yml)

[Манифест ingress](https://github.com/loginochka/kuber/blob/main/h-10/nginx-chart/templates/ingress.yml)

[Манифест service](https://github.com/loginochka/kuber/blob/main/h-10/nginx-chart/templates/service.yml)

[Манифест configmap](https://github.com/loginochka/kuber/blob/main/h-10/nginx-chart/templates/configmap.yml)
