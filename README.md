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
- Проверена работа web сервера развернутого из манифеста web-pod.yaml с помощью `kubectl port-forward --address 0.0.0.0 pod/web 8000:8000`
- Сoredns восстанавливается, т.к. управляется через Deployment который при развернтвании автоматитчески создает соответствующий ReplicaSet.
