# Back-end
Lista de presença digitalizada.
controle-de-acesso-web-api — Backend (Spring Boot)

API desenvolvida em Spring Boot para o sistema Controle-de-Acesso-Web, responsável por autenticação, cadastro de escolas/turmas/alunos e registro de presença por lista assistida.
Fornece endpoints seguros para integração com o app móvel (React Native) e painel web, além de gerar alertas automáticos e relatórios de frequência.

🧩 Tecnologias Principais
Categoria	Stack
Linguagem	Java 21
Framework	Spring Boot 3 (Web, Security, Data JPA, Validation)
Banco de Dados	PostgreSQL 15+
Cache	Redis (opcional)
Autenticação	JWT + Refresh Token
Infraestrutura	Docker, GitHub Actions, Azure Boards
🚀 Objetivo

Oferecer uma API robusta e segura para digitalizar o controle de presença escolar, reduzindo falhas manuais e permitindo acompanhamento em tempo real por gestores.

🧠 Principais Endpoints
Método	Endpoint	Descrição
POST	/auth/login	Autenticação e geração de token
GET	/schools, /classes, /students	Cadastros base
POST	/lessons/{id}/attendance/bulk	Registro de presenças (lista assistida)
PATCH	/lessons/{id}/attendance/{studentId}	Atualização rápida de presença
GET	/reports/attendance	Relatórios de frequência
GET	/alerts/recent	Alertas automáticos
⚙️ Como Rodar o Projeto
📦 Pré-requisitos

Java 21

Maven 3.9+

PostgreSQL 15+

▶️ Executar
mvn spring-boot:run
🐳 Com Docker
docker build -t controle-api .
docker run -p 8080:8080 controle-api
🧾 Licença

Distribuído sob licença MIT. Consulte o arquivo LICENSE para mais detalhes.

🧭 Links

🔗 App Frontend: controle-de-acesso-web-app

🗂️ Azure Boards: integração via AB#<id> nos commits
