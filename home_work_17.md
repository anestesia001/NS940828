1) Установить minikube
2) Написать манифест пода, который запускает контейнер из image alpine
3) Проверить, что pod запустился, посмотреть информацию о поде и логи контейнера
4) Создать манифест `httpd.yaml`
```yaml
apiVersion: v1
kind: Pod
metadata:
  name: broken-web
spec:
  containers:
    - name: web
      image: httpd:wrong-tag
```
применить его, найти ошибку и исправить ее

5) Создать namespace dev
6) Запустить поды из п2 и п4 в namespace dev
