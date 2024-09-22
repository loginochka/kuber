# Запуск приложений в K8S

## Задание 1. Создать Deployment и обеспечить доступ к репликам приложения из другого Pod

1. Создать Deployment приложения, состоящего из двух контейнеров — nginx и multitool. Решить возникшую ошибку.
2. После запуска увеличить количество реплик работающего приложения до 2.
3. Продемонстрировать количество подов до и после масштабирования.
4. Создать Service, который обеспечит доступ до реплик приложений из п.1.
5. Создать отдельный Pod с приложением multitool и убедиться с помощью curl, что из пода есть доступ до приложений из п.1.

---

## Ответ 

[Манифест](https://github.com/loginochka/kuber/blob/main/h-3/13-1-deployment.yml)

![Масштабирование](https://github.com/loginochka/kuber/blob/main/media/1_3_rs_after_update.png)

![Результат curl`а](https://github.com/loginochka/kuber/blob/main/media/1_3_check_connection_inside.png)

---

## Задание 2. Создать Deployment и обеспечить старт основного контейнера при выполнении условий

1. Создать Deployment приложения nginx и обеспечить старт контейнера только после того, как будет запущен сервис этого приложения.
2. Убедиться, что nginx не стартует. В качестве Init-контейнера взять busybox.
3. Создать и запустить Service. Убедиться, что Init запустился.
4. Продемонстрировать состояние пода до и после запуска сервиса.

---

## Ответ 

[Манифест Deployment`а](https://github.com/loginochka/kuber/blob/main/h-3/13-2-deployment.yml)

[Манифест Service`а](https://github.com/loginochka/kuber/blob/main/h-3/13-2-service.yml)

![Резултат работы до и после запуска сервиса](https://github.com/loginochka/kuber/blob/main/media/1_3_init_container.png)
