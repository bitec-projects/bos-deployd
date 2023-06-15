# 19-abr-2023

Bier - Subi para o Github o repositório do deployd-plus, com ajustes no mongodb client para nova versão (estava dando incompatibilidade com mongo Atlas);
Esse repositório está publicado no pacote deployd-plus do npm e é o repositório válido para os projetos Referenceit

# 24-abr-2023

Bier - No arquivo .env, é necessário configurar os seguintes parâmetros:
REQUESTTIMEOUT - timeout para requisições http
DEPLOYD_APP_PORT - porta que receberá conexões
ENVIRONMENT - ambiente que será publicado na pasta public-development ou public-production
MONGO_CONNECTION_STRING - connection string do servidor mongodb.
MONGO_DATABASE - nome do database que será conectado

# 26-abr-2023

Bier

-   Removido recurso para conexão em mongo sem connectionString;
-   Ajustando configurações para ter compatibilidade com futuras versão do Bos, exemplo de configurações para criação do object bosDeployd:
---
    return bosDeployd({
        port: process.env.DEPLOYD_APP_PORT || 80,
        env: process.env.ENVIRONMENT || 'development',
        requestTimeout: parseInt(process.env.REQUESTTIMEOUT) || 10000,
        db: {
            mongoConnectionString: process.env.MONGO_CONNECTION_STRING || '',
            mongoDatabaseName: process.env.MONGO_DATABASE_NAME
        }
    });
---

# 15-jun-2023

Bier

- Adicionado recursos de $ignoreLimitRecursion que estava ausente.