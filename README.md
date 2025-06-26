# 🔐 AutheticUser - API de Autenticação com JWT

Esta API foi construída com Spring Boot e implementa autenticação baseada em **JWT (JSON Web Token)**. Abaixo estão as instruções para executar o projeto localmente, acessar recursos úteis e realizar testes de desempenho com JMeter.

---

## ✅ Pré-requisitos

- Java 17 ou superior  
- Maven instalado  
- JMeter (opcional, para testes de carga)

---

## 🚀 Como executar o projeto

1. Clone o repositório:

```bash
git clone git@github.com:gabrielecastro/arquitetura-web.git
cd ApiValidacaoJwt-main/autheticuser
Compile o projeto com Maven:

bash
Copiar
Editar
mvn clean install
Inicie a aplicação:

bash
Copiar
Editar
mvn spring-boot:run
A API estará disponível em: http://localhost:8080

📄 Documentação Swagger
A documentação interativa pode ser acessada em:

👉 http://localhost:8080/swagger-ui/index.html#/Autenticação/login

Para testar o login, utilize o endpoint POST /auth/login com o seguinte corpo JSON:

json
Copiar
Editar
{
  "username": "admin",
  "password": "123456"
}
🗃️ Console H2
Para visualizar o banco em memória (H2), acesse:

👉 http://localhost:8080/h2-console

Credenciais de acesso:

JDBC URL: jdbc:h2:mem:testdb

Usuário: gustavo

Senha: 123456

🧪 Testes de carga com JMeter
Configuração no JMeter:
Criar novo plano de teste:
File > New

Adicionar Thread Group:
Test Plan > Add > Threads (Users) > Thread Group

Número de usuários: 200

Ramp-up: 20 segundos

Loop Count: 10 ou marque Forever para testar continuamente

Adicionar requisição HTTP:
Thread Group > Add > Sampler > HTTP Request

Método: POST

Caminho: /auth/login

Servidor: localhost

Porta: 8080

Body da requisição:

json
Copiar
Editar
{
  "username": "admin",
  "password": "123456"
}
Adicionar cabeçalho HTTP:
Login Request > Add > Config Element > HTTP Header Manager

Content-Type: application/json

Para visualizar resultados:
Thread Group > Add > Listener > View Results Tree

✅ Pronto! Agora você tem uma API JWT funcional com autenticação, console de banco, documentação Swagger e suporte para testes de carga.


