# All in Market

Набор чартов для деплоя ELK, Kafka, Monitoring и PostgreSQL в Kubernetes.

---

## 📦 ELK Stack
### Установка
```bash
helm dependency build .\k8s\elk-chart\
helm install elk .\k8s\elk-chart\ -n logging --create-namespace
```

Обновление зависимостей
```bash
helm dependency update .\k8s\elk-chart\
```

Удаление
```bash
helm uninstall elk -n logging
```

---

## 📦 Kafka
### Установка
```bash
helm dependency build .\k8s\kafka-chart\
helm install kafka .\k8s\kafka-chart\ -n kafka --create-namespace
```

Обновление зависимостей
```bash
helm dependency update .\k8s\kafka-chart\
```

Удаление
```bash
helm uninstall kafka -n kafka
```

---

## 📦 Monitoring (Prometheus + Grafana
### Установка
```bash
helm dependency build .\k8s\monitoring-chart\
helm install monitoring .\k8s\monitoring-chart\ -n monitoring --create-namespace
```

Обновление зависимостей
```bash
helm dependency update .\k8s\monitoring-chart\
```

Удаление
```bash
helm uninstall monitoring -n monitoring
```

---

## 📦 Postgresql
### Установка
```bash
helm install postgresql .\k8s\postgresql-chart\ -n postgresql --create-namespace
```

Обновление зависимостей
```bash
helm dependency update .\k8s\postgresql-chart\
```

Удаление
```bash
helm uninstall postgresql -n postgresql
```