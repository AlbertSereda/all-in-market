Создание configmap с инициализацией БД для сервисов для PostgreSQL:

kubectl create configmap postgres-initdb-config --from-file=init-db.sql=./init-scripts/init-db.sql


Команда установки ELK helm:

helm dependency build .\k8s\elk-chart\

helm install elk .\k8s\elk-chart\ -n logging --create-namespace

Команда установки Kafka helm:

helm dependency build .\k8s\kafka-chart\

helm install kafka .\k8s\kafka-chart\ -n kafka --create-namespace