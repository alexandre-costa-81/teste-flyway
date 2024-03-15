# Teste flyway

É um projeto para demonstrar o uso do flaway.

Exemplo retirado de https://www.mastertheboss.com/various-stuff/flyway/getting-started-with-flyway/

## Passo a Passo

Levantar uma aplicação postgres localmente com o Docker:

```
docker run --rm=true --name flyway_test -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=postgres -e POSTGRES_DB=postgres -p 6543:5432 postgres
```
Agora vamos realizar a migração propriamente dita. Antes disso, recomendamos verificar se sua configuração de migração está correta e ver as migrações disponíveis. Você pode fazer isso com o objetivo "info":

```
mvn flyway:info
```

Para executar a migrate use o seguinte comando:

```
mvn flyway:migrate
```

Por hoje é só!
