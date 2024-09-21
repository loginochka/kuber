# Базовые объекты K8S

## Задание 1. Создать Pod с именем hello-world

1. Создать манифест (yaml-конфигурацию) Pod.
2. Использовать image - gcr.io/kubernetes-e2e-test-images/echoserver:2.2.
3. Подключиться локально к Pod с помощью kubectl port-forward и вывести значение (curl или в браузере).

## Ответ 

![curl до Pod](https://github.com/loginochka/kuber/blob/main/media/1_2_curl_pod.png)

[Манифест Pod`a](https://github.com/loginochka/kuber/blob/main/h-2/ex-pod.yml)

## Задание 2. Установка и настройка локального kubectl

1. Создать Pod с именем netology-web.
2. Использовать image — gcr.io/kubernetes-e2e-test-images/echoserver:2.2.
3. Создать Service с именем netology-svc и подключить к netology-web.
4. Подключиться локально к Service с помощью kubectl port-forward и вывести значение (curl или в браузере).

## Ответ 

![curl до Service](https://github.com/loginochka/kuber/blob/main/media/1_2_curl_svc.png)

[Манифест Service`a](https://github.com/loginochka/kuber/blob/main/h-2/ex-service.yml)