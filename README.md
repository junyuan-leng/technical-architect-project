## Django-Postgres-K8s-Deployment

### Deploy Postgres

1. Add Postgres Secret

    ```
	kubectl apply -f postgres/postgres-secret.yaml
    ```

2. Create Postgres Storage Volume

    ```
	kubectl apply -f postgres/postgres-volume.yaml
    ```

3. Deploy Postgres

    ```
	kubectl apply -f postgres/postgres-deployment.yaml
    ```

4. Expose Postgres Service

    ```
	kubectl apply -f postgres/postgres-service.yaml
    ```

### Deploy Django

1. Add Django Secret

    ```
	kubectl apply -f django/django-secret.yaml
    ```

2. Deploy Django

    ```
	kubectl apply -f django/django-deployment.yaml
    ```

3. Expose Django Service

    ```
	kubectl apply -f django/django-service.yaml
    ```