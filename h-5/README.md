# Сетевое взаимодействие в K8S. Часть 2

## Задание 1. Создать Deployment приложений backend и frontend

1. Создать Deployment приложения _frontend_ из образа nginx с количеством реплик 3 шт.
2. Создать Deployment приложения _backend_ из образа multitool. 
3. Добавить Service, которые обеспечат доступ к обоим приложениям внутри кластера. 
4. Продемонстрировать, что приложения видят друг друга с помощью Service.
5. Предоставить манифесты Deployment и Service в решении, а также скриншоты или вывод команды п.4.

---

## Ответ 

[Манифест Deployment`а](https://github.com/loginochka/kuber/blob/main/h-5/15-1-deployment.yml)

[Манифест Service`а](https://github.com/loginochka/kuber/blob/main/h-5/15-1-service.yml)

![curl из Pod`ов](https://github.com/loginochka/kuber/blob/main/media/1_5_curl_app.png)

---

## Задание 2. Создать Ingress и обеспечить доступ к приложениям снаружи кластера

1. Включить Ingress-controller в MicroK8S.
2. Создать Ingress, обеспечивающий доступ снаружи по IP-адресу кластера MicroK8S так, чтобы при запросе только по адресу открывался _frontend_ а при добавлении /api - _backend_.
3. Продемонстрировать доступ с помощью браузера или `curl` с локального компьютера.
4. Предоставить манифесты и скриншоты или вывод команды п.2.

---

## Ответ 

[Манифест ingress`а](https://github.com/loginochka/kuber/blob/main/h-5/15-1-ingress.yml)

![curl DNS кластера](https://github.com/loginochka/kuber/blob/main/media/1_5_curl_ingress.png)
