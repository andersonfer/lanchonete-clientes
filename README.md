# Lanchonete Clientes

Microserviço de gestão de clientes do sistema de lanchonete.

## Tecnologias

- Java 17
- Spring Boot 3
- Spring JDBC
- MySQL (RDS)
- Docker
- Kubernetes (EKS)

## Funcionalidades

- Cadastro de clientes
- Identificação por CPF
- Consulta de clientes

## Endpoints

| Método | Endpoint | Descrição |
|--------|----------|-----------|
| POST | `/clientes` | Cadastrar cliente |
| GET | `/clientes/cpf/{cpf}` | Buscar cliente por CPF |
| POST | `/clientes/identificar` | Identificar cliente |
| GET | `/actuator/health` | Health check |

## Executar Localmente

```bash
# Compilar
mvn clean package

# Executar
java -jar target/clientes-1.0.0.jar
```

## Testes

```bash
# Executar testes
mvn test

# Gerar relatório de cobertura
mvn jacoco:report
```

## Docker

```bash
# Build
docker build -t lanchonete-clientes .

# Run
docker run -p 8080:8080 lanchonete-clientes
```

## Deploy

O deploy é automatizado via GitHub Actions:
- **CI**: Executado em Pull Requests (testes + SonarCloud)
- **CD**: Executado no merge para main (build + deploy no EKS)

## Repositórios Relacionados

- [lanchonete-infra](https://github.com/andersonfer/lanchonete-infra) - Infraestrutura
- [lanchonete-pedidos](https://github.com/andersonfer/lanchonete-pedidos)
- [lanchonete-cozinha](https://github.com/andersonfer/lanchonete-cozinha)
- [lanchonete-pagamento](https://github.com/andersonfer/lanchonete-pagamento)
