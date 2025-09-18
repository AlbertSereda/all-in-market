Создание configmap с инициализацией БД для сервисов для PostgreSQL:

kubectl create configmap postgres-initdb-config --from-file=init-db.sql=./init-scripts/init-db.sql