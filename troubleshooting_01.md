# Minimal CMDB

Минимальная CMDB: CI (configuration items) с CRUD-функциями, поиском и PostgreSQL. Frontend и backend — отдельные Python-сервисы под systemd:
- cmdb-backend.service
- cmdb-frontend.service

postgres развернут на машине с backend`ом
## backend

```bash
curl http://127.0.0.1:8000/health
curl http://127.0.0.1:8000/api/v1/configuration-items
```

## frontend

```bash
curl 127.0.0.1:8080
curl 127.0.0.1:8080/docs
```
