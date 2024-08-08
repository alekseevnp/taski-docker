# taski-docker
`docker compose up` и полетели

## Не забываем собрать статику...
`docker compose exec backend python manage.py collectstatic`
`docker compose exec backend cp -r /app/collected_static/. /backend_static/static/`

## Production
Запуск
`docker compose -f docker-compose.production.yml up -d`

Миграции
`docker compose -f docker-compose.production.yml exec backend python manage.py migrate`

Статика
`docker compose -f docker-compose.production.yml exec backend python manage.py collectstatic`
`docker compose -f docker-compose.production.yml exec backend cp -r /app/collected_static/. /backend_static/static/`