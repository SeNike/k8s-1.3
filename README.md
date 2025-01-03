# Домашнее задание к занятию «Запуск приложений в K8S»

### Задание 1. Создать Deployment и обеспечить доступ к репликам приложения из другого Pod

1. Создать [Deployment](https://github.com/SeNike/k8s-1.3/blob/main/deployment.yaml) приложения, состоящего из двух контейнеров — nginx и multitool. Решить возникшую ошибку.

![IMG](https://github.com/SeNike/Study_24/blob/main/k8s/1.3/1.png)

![IMG](https://github.com/SeNike/Study_24/blob/main/k8s/1.3/2.png)

![IMG](https://github.com/SeNike/Study_24/blob/main/k8s/1.3/3.png)

2. После запуска увеличить количество реплик работающего приложения до 2.

![IMG](https://github.com/SeNike/Study_24/blob/main/k8s/1.3/4.png)

3. Продемонстрировать количество подов до и после масштабирования.
4. Создать [Service](https://github.com/SeNike/k8s-1.3/blob/main/nginx-multitool-service.yaml), который обеспечит доступ до реплик приложений из п.1.
5. Создать отдельный [Pod](https://github.com/SeNike/k8s-1.3/blob/main/multitool-pod.yaml) с приложением multitool и убедиться с помощью `curl`, что из пода есть доступ до приложений из п.1.

![IMG](https://github.com/SeNike/Study_24/blob/main/k8s/1.3/5.png)

------

### Задание 2. Создать Deployment и обеспечить старт основного контейнера при выполнении условий

1. Создать [Deployment](https://github.com/SeNike/k8s-1.3/blob/main/nginx-deployment.yaml) приложения nginx и обеспечить старт контейнера только после того, как будет запущен сервис этого приложения.
2. Убедиться, что nginx не стартует. В качестве Init-контейнера взять busybox.
3. Создать и запустить [Service](https://github.com/SeNike/k8s-1.3/blob/main/nginx-service.yaml). Убедиться, что Init запустился.
4. Продемонстрировать состояние пода до и после запуска сервиса.

![IMG](https://github.com/SeNike/Study_24/blob/main/k8s/1.3/6.png)

