# Eureka Server (Service Registry)

Serviço de registro e descoberta de instâncias para a arquitetura de microsserviços.

## Configurações Principais

- **Porta**: 8761
- **Profiles**: `default`, `local`, `prod`
- **Spring Boot**: 3.5.7 (Kotlin 2.2.21)
- **JDK**: 24

## Funcionalidades

- **Service Registry**: Ponto central onde todos os serviços se registram.
- **Service Discovery**: Permite que serviços encontrem uns aos outros via nome de aplicação (ex: `lb://face-recognition-api`).
- **Swagger UI**: Disponível em `/` (via Springdoc).
- **Auto-Preservation**: Configurado para manter instâncias mesmo em caso de falhas de rede temporárias.

## Endpoints de Monitoramento

- `/actuator/health`: Status de saúde do servidor.
- `/actuator/info`: Informações gerais.

## Dependências Relevantes

- `spring-cloud-starter-netflix-eureka-server`
- `springdoc-openapi-starter-webmvc-ui`
- `logstash-logback-encoder`
