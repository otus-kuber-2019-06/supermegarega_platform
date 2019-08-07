# supermegarega_platform
supermegarega Platform repository

# homework-1 Знакомство с Kubernetes.

- Установлен kubectl при помощи Homebrew - `brew install kubernetes-cli`.
- Настроен Kubectl Autocomplete для bash.
- Установлен minicube при помощи Homebrew - `brew cask install minikube`.
- Установлен Web UI Dashboard для Kubernetes.
- Установлен k9s для визуализации консольной работы - `brew install derailed/k9s/k9s`.
- Создан docker образ с Nginx и загружен на hub.docker.com smrdevops/nginx-alpine:1.0.
- Создан и применен манифест web-pod.yaml.
- Проверена работа web сервера развернутого из манифеста web-pod.yaml с помощью `kubectl port-forward --address 0.0.0.0 pod/web 8000:8000`.
- Сoredns восстанавливается, т.к. управляется через Deployment который при развернтвании автоматитчески создает соответствующий ReplicaSet.

# homework-2 Безопасность в Kubernetes.

`task01`
- Создан Service Account bob с ролью admin в рамках всего кластера.
- Создан Service Account dave без доступа к кластеру.

`task02`
- Создан Namespace prometheus.
- Создан Service Account carol в Namespace prometheus.
- Всем Service Account в Namespace prometheus дана возможность делать get, list, watch в отношении Pods всего
кластера.

`task03`
- Создан Namespace dev.
- Создан Service Account jane в Namespace dev.
- Выдана роль admin пользователю jane в рамках Namespace dev.
- Создан Service Account ken в Namespace dev.
- Выдана роль view пользователю ken в рамках Namespace dev.

# homework-3 Сетевое взаимодействие kubernetes.

- Добавлены проверки pod-ов readinessProbe и livenessProbe.
- Создан Deployment для обновления конфигурации pod-ов.
- Создан сервис ClusterIP.
- Для kube-proxy включен режим работы IPVS.
- Установлен MetalLb.
- Настроен доступ к CoreDNS.
- Настроен Ingress контроллер ingress-nginx.
- Настроено подключение приложение Web к Ingress.
