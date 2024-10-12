# Домашнее задание к занятию «Конфигурация приложений»

### Задание 1. Создать Deployment приложения и решить возникшую проблему с помощью ConfigMap. Добавить веб-страницу

1. Создать Deployment приложения, состоящего из контейнеров nginx и multitool.
2. Решить возникшую проблему с помощью ConfigMap.
3. Продемонстрировать, что pod стартовал и оба конейнера работают.
4. Сделать простую веб-страницу и подключить её к Nginx с помощью ConfigMap. Подключить Service и показать вывод curl или в браузере.
5. Предоставить манифесты, а также скриншоты или вывод необходимых команд.

---

### Ответ 1 

[Манифест Deployment](https://github.com/loginochka/kuber/blob/main/h-8/23-dpl.yml)

[Манифест Service](https://github.com/loginochka/kuber/blob/main/h-8/23-svc.uml)

[Манифест Ingress](https://github.com/loginochka/kuber/blob/main/h-8/23-ing.yml)

[Манифест ConfigMap](https://github.com/loginochka/kuber/blob/main/h-8/23-cm.yml)

![Результат](https://github.com/loginochka/kuber/tree/main/media/2_3_custom_nginx.png)

---

### Задание 2. Создать приложение с вашей веб-страницей, доступной по HTTPS 

1. Создать Deployment приложения, состоящего из Nginx.
2. Создать собственную веб-страницу и подключить её как ConfigMap к приложению.
3. Выпустить самоподписной сертификат SSL. Создать Secret для использования сертификата.
4. Создать Ingress и необходимый Service, подключить к нему SSL в вид. Продемонстировать доступ к приложению по HTTPS. 
4. Предоставить манифесты, а также скриншоты или вывод необходимых команд.

---

[Манифест Deployment](https://github.com/loginochka/kuber/blob/main/h-8/23-dpl-nginx.yml)

[Манифест Service](https://github.com/loginochka/kuber/blob/main/h-8/23-svc.uml)

[Манифест Ingress](https://github.com/loginochka/kuber/blob/main/h-8/23-ing.yml)

[Манифест ConfigMap](https://github.com/loginochka/kuber/blob/main/h-8/23-cm-tls.yml)

[Манифест Secret](https://github.com/loginochka/kuber/blob/main/h-8/23-sec.yml)

![Результат](https://github.com/loginochka/kuber/tree/main/media/2_3_https_ingres.png)
