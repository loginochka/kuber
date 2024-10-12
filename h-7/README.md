# Хранение в K8s. Часть 2

## Задание 1.

**Что нужно сделать**

Создать Deployment приложения, использующего локальный PV, созданный вручную.

1. Создать Deployment приложения, состоящего из контейнеров busybox и multitool.
2. Создать PV и PVC для подключения папки на локальной ноде, которая будет использована в поде.
3. Продемонстрировать, что multitool может читать файл, в который busybox пишет каждые пять секунд в общей директории. 
4. Удалить Deployment и PVC. Продемонстрировать, что после этого произошло с PV. Пояснить, почему.
5. Продемонстрировать, что файл сохранился на локальном диске ноды. Удалить PV.  Продемонстрировать что произошло с файлом после удаления PV. Пояснить, почему.
5. Предоставить манифесты, а также скриншоты или вывод необходимых команд.

---

## Ответ 

[Манифест Deployment](https://github.com/loginochka/kuber/blob/main/h-7/22-deployment.yml)

[Манифест pv](https://github.com/loginochka/kuber/blob/main/h-7/22-pv.yml)

![multitool может читать файл](https://github.com/loginochka/kuber/blob/main/media/2_2_check_log_dep.png)

После удаления Deployment и PVC, pv остается, так как выставлена политика _ReclaimPolicy: Retain_

![Удаленный pvc и Deployment](https://github.com/loginochka/kuber/blob/main/media/2_2_pv_after_delete.png)

![Файл на pv](https://github.com/loginochka/kuber/blob/main/media/2_2_pv_file.png)

После удаления PV, данные на диске не будут автоматически удалены, так как Kubernetes не управляет данными вне своих абстракций

---

## Задание 2.

**Что нужно сделать**

Создать Deployment приложения, которое может хранить файлы на NFS с динамическим созданием PV.

1. Включить и настроить NFS-сервер на MicroK8S.
2. Создать Deployment приложения состоящего из multitool, и подключить к нему PV, созданный автоматически на сервере NFS.
3. Продемонстрировать возможность чтения и записи файла изнутри пода. 
4. Предоставить манифесты, а также скриншоты или вывод необходимых команд.

---

## Ответ 

NFS-сервер разернут на 1 ноде. На 2 и 3 нодах установлен nfs-клиент. В качестве provisioner используется nfs-subdir-external-provisioner

[Манифест Deployment](https://github.com/loginochka/kuber/blob/main/h-6/22-deployment-nfs.yml)

[Манифест PVC](https://github.com/loginochka/kuber/blob/main/h-6/22-pvc.yml)

![Результат из ноды](https://github.com/loginochka/kuber/blob/main/media/2_2_nfs_check_in_node.png)

![Результат из пода](https://github.com/loginochka/kuber/blob/main/media/2_2_nfs_rw_check.png)
