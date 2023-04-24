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
