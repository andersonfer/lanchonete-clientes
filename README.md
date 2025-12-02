# Lanchonete - Clientes

Microsserviço responsável pelo cadastro e identificação de clientes.

## Tecnologias

- Java 17
- Spring Boot 3
- MySQL (RDS)
- RabbitMQ

## Endpoints

| Método | Endpoint | Descrição |
|--------|----------|-----------|
| POST | /clientes | Cadastrar novo cliente |
| POST | /clientes/identificar | Identificar cliente por CPF |
| GET | /clientes/cpf/{cpf} | Buscar cliente por CPF |

## Executar Localmente

```bash
mvn spring-boot:run
```

## Testes

```bash
mvn test
```

## Cobertura

[![Coverage](https://sonarcloud.io/api/project_badges/measure?project=andersonfer_lanchonete-clientes&metric=coverage)](https://sonarcloud.io/project/overview?id=andersonfer_lanchonete-clientes)
