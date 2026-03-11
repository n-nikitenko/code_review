Install

```bash
pip install -e .
```

Run Postgres (Docker)

```bash
cp .env.example .env
docker compose up -d
```

Configure env:
```bash
set -a
source .env
set +a
```

Apply migrations
```bash
alembic upgrade head
```

Run

```bash
uvicorn --factory app.main:create_app
```
