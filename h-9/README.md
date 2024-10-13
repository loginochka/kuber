# Домашнее задание к занятию "Управление доступом"

### Задание 1. Создайте конфигурацию для подключения пользователя

1. Создайте и подпишите SSL-сертификат для подключения к кластеру.
2. Настройте конфигурационный файл kubectl для подключения.
3. Создайте роли и все необходимые настройки для пользователя.
4. Предусмотрите права пользователя. Пользователь может просматривать логи подов и их конфигурацию (`kubectl logs pod <pod_id>`, `kubectl describe pod <pod_id>`).
5. Предоставьте манифесты и скриншоты и/или вывод необходимых команд.
---

### Ответ 1 

[Манифест Role](https://github.com/loginochka/kuber/blob/main/h-9/24-pod-reader-role.yaml)

[Манифест RoleBinding](https://github.com/loginochka/kuber/blob/main/h-9/24-read-pods-binding.yaml)


![Результат](https://github.com/loginochka/kuber/blob/main/media/2_4_user_context.png)
