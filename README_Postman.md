# Testes de API - Postman | Quality Eagles - Academy #13

Este projeto faz parte do programa de formação **QA Coders Academy #13** da QAcoders, e tem como objetivo a criação e execução de testes de API utilizando o **Postman**.

## 🚀 Sobre o Projeto

A coleção de testes cobre os principais endpoints da API disponibilizada no desafio, com foco nas entidades **User** e **Company**, incluindo cenários **positivos e negativos**, além de testes de **autenticação (login)**.

---

## 🔐 Autenticação

- Login com e-mail e senha válidos  
- Validação de campos obrigatórios  
- Testes de login com dados inválidos  
- **Status code 200** para login válido  
- **Status code 403** para login inválido ou acesso proibido  

---

## 👤 Usuário (User)

- Listar todos os usuários  
- Consultar dados de usuário por ID  
- Criar novo usuário  
- Atualizar dados do usuário por ID  
- Excluir usuário  
- Testes com campos obrigatórios ausentes  
- Validação de dados inválidos  

---

## 🏢 Empresa (Company)

- Criar nova empresa  
- Listar empresas registradas  
- Contar total de empresas (`GET /company/count`)  
- Atualizar dados da empresa por ID  
- Consultar empresa por ID  
- Deletar empresa por ID  
- Testes com dados inválidos ou campos obrigatórios vazios  

---

## ✅ Validações dos Testes

Durante a execução dos testes automatizados no Postman, são feitas diversas validações, como:

- **Status Code 200** para requisições de sucesso (GET, PUT, DELETE)  
- **Status Code 201 - Created** para criação de dados  
- **Mensagens de sucesso** no corpo da resposta (body)  
- **Nome da empresa** presente na resposta  
- Empresa criada com `"status": true`  
- **E-mail da empresa** deve conter o caractere `@`  
- **Status Code 403** para acessos não autorizados  
- Mensagem `"No tests found"` para endpoints ainda não validados  

---

## 🛠 Tecnologias Utilizadas

- Postman  
- Newman (execução via terminal)  
- Git e GitHub  

---

## 📁 Estrutura do Projeto

```
MeuProjetoPostman/
├── postman/
│   └── Quality-Eagles.postman_collection.json
├── README.md
```

---

## ▶️ Como Executar os Testes

### No Postman:

1. Clone este repositório:
   ```bash
   git clone https://github.com/iza975/Testes-api-postman-quality-eagles-academy13-api-postman.git
   cd Testes-api-postman-quality-eagles-academy13-api-postman
   ```

2. No Postman:
   - Clique em **Importar**
   - Selecione o arquivo: `postman/Quality-Eagles.postman_collection.json`
   - Execute a coleção de testes

### Via terminal com Newman (opcional):

1. Instale o Newman:
   ```bash
   npm install -g newman
   ```

2. Execute a coleção:
   ```bash
   newman run postman/Quality-Eagles.postman_collection.json
   ```

---

## 👩‍💻 Desenvolvido por

**Sônia Izabel Wicki**  
Aluna QA Coders Academy #13  
📍 Almirante Tamandaré - PR

💡 Este projeto foi desenvolvido por Sônia Izabel Wicki, que acredita que a tecnologia transforma, a qualidade sustenta e o aprendizado contínuo impulsiona a evolução.