# taski-docker
`docker compose up` и полетели

## Не забываем собрать статику...
`docker compose exec backend python manage.py collectstatic`
`docker compose exec backend cp -r /app/collected_static/. /backend_static/static/`