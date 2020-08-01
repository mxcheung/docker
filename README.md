# docker
docker build secret

echo "mysupersecretpassword" | docker secret create pg_password -
echo "mydatabase" | docker secret create pg_database -

https://dzone.com/articles/introduction-to-docker-secrets

        environment:
            POSTGRES_USER_FILE: /run/secrets/pg_user
            POSTGRES_PASSWORD_FILE: /run/secrets/pg_password
            POSTGRES_DB_FILE: /run/secrets/pg_database
        secrets:
           - pg_password
           - pg_user
           - pg_database


https://gist.github.com/aramalipoor/f62355cd440584986bfd91bd69e52c49
