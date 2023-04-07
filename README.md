# Step by step


## Build Docker images for FastAPI and for PostgreSQL

```
docker build -t fastapi-image -f Dockerfile.fastapi .

docker build -t postgres-image -f Dockerfile.postgresql .
```

## Build container and use it



```
docker-compose build

docker-compose up
```

## Check if it's working



### Start fastapi container

```
docker-compose exec fastapi sh
```

### Run python

```
python
```

### Try to connect to PostgreSQL
```
import psycopg2
conn = psycopg2.connect(host="postgres", port=5432, dbname="fastapi_db", user="admin", password="password")
```

