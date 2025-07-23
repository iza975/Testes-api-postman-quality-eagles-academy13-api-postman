# Testes de API - Postman | Quality Eagles - Academy 13

Este projeto faz parte do programa de formação QA Coders Academy  da QAcoders, com o objetivo de criar e executar testes de API utilizando o Postman. A execução automatizada dos testes é realizada através de Integração Contínua com GitHub Actions.


<!-- ![Status dos Testes](https://img.shields.io/github/actions/workflow/status/iza975/Testes-api-postman-quality-eagles-academy13-api-postman/postman-tests.yml?branch=main&label=Status%20dos%20Testes&style=for-the-badge) -->


 Sobre o Projeto

A coleção de testes cobre os principais endpoints da API disponibilizada no desafio, com foco nas entidades User e Company, incluindo cenários positivos e negativos, além de testes de autenticação (login).

---

 Autenticação

- Login com e-mail e senha válidos  
- Validação de campos obrigatórios  
- Testes de login com dados inválidos  
- **Status Code 200** para login válido  
- **Status Code 403** para login inválido ou acesso proibido  

---

 Usuário (User)

- Listar todos os usuários  
- Consultar dados de usuário por ID  
- Criar novo usuário  
- Atualizar dados do usuário por ID  
- Excluir usuário  
- Testes com campos obrigatórios ausentes  
- Validação de dados inválidos  

---

 Empresa (Company)

- Criar nova empresa  
- Listar empresas registradas  
- Contar total de empresas  
- Atualizar dados da empresa por ID  
- Consultar empresa por ID  
- Deletar empresa por ID  
- Testes com dados inválidos ou campos obrigatórios vazios  

---

 Validações dos Testes

Durante a execução dos testes automatizados no Postman, são feitas diversas validações, como:

- Status Code 200 para requisições de sucesso (GET, PUT, DELETE)  
- Status Code 201 (Created) para criação de dados  
- Mensagens de sucesso no corpo da resposta (body)  
- Nome da empresa presente na resposta  
- Empresa criada com `"status": true`  
- E-mail da empresa deve conter o caractere `@`  
- Status Code 403 para acessos não autorizados  
- Mensagem `No tests found` para endpoints ainda não validados  

---

 Tecnologias Utilizadas

- Postman  
- Newman (execução via terminal)  
- Git e GitHub
Integração Contínua com GitHub Actions
A execução automatizada dos testes via GitHub Actions é realizada no fluxo de push ou pull request na branch main. 

---

 Estrutura do Projeto

```
MeuProjetoPostman/
├── postman/
│   └── Quality-Eagles.postman_collection.json
├── README.md
```

---

 Como Executar os Testes

 No Postman:

1. Clone este repositório:
   ```bash
   git clone https://github.com/iza975/Testes-api-postman-quality-eagles-academy13-api-postman.git
   cd Testes-api-postman-quality-eagles-academy13-api-postman
   ```

2. No Postman:
   - Clique em **Importar**
   - Selecione o arquivo: `postman/Quality-Eagles.postman_collection.json`
   - Execute a coleção de testes

 Via terminal com Newman (opcional):

1. Instale o Newman:
   ```bash
   npm install -g newman
   ```

2. Execute a coleção:
   ```bash
   newman run postman/Quality-Eagles.postman_collection.json
   ```

---

Este projeto foi desenvolvido por Sônia Izabel Wicki, participante do QA Coders Academy 13, que acredita que a tecnologia transforma, a qualidade é indispensável e o aprendizado contínuo impulsiona a evolução.


---


Observações

Este projeto foi desenvolvido durante o programa QA Coders Academy 13, utilizando uma API fornecida pela própria Academy.

Com o passar do tempo, a API pode ter sofrido alterações (como exclusão, mudança ou proteção de endpoints), o que pode resultar em falhas nos testes automatizados (ex: erro 404 ou problemas de certificado SSL).

O código original foi mantido como forma de demonstrar o conhecimento em testes de API com Postman, integração contínua com GitHub Actions, e boas práticas de versionamento e documentação.


