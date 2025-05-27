# 📦 Refund API

API para um sistema de reembolso com autenticação e controle de permissão por tipo de usuário.

## 🚀 Tecnologias Utilizadas

- Node.js
- Express
- Prisma
- SQLite
- JWT 
- TypeScript


## 🔧 Instalação

Siga estes passos para configurar o ambiente de desenvolvimento:

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/MarlonChi/api-refund](https://github.com/MarlonChi/api-refund)
    cd api-refund
    ```

2.  **Instale as dependências:**
    ```bash
    npm install
    # ou
    yarn install
    ```

3.  **Configuração das Variáveis de Ambiente:**
    Crie um arquivo `.env` na raiz do projeto com base no arquivo `.env.example`.

4.  **Iniciar o Servidor:**
    ```bash
    npm start
    # ou
    yarn start
    ```

    A API estará rodando em `http://localhost:3333` (ou pela porta configurada no seu `.env`).

## 🗺️ Rotas da API

Para uma visão rápida dos endpoints disponíveis, seus métodos HTTP, requisitos de autenticação e os papéis de usuário necessários para acessá-los, consulte a tabela abaixo:

| Rota                    | Descrição                                         | Método HTTP | Autenticação             | Role (Papel de Acesso)           |
| :---------------------- | :------------------------------------------------ | :---------- | :----------------------- | :------------------------------- |
| `/users`                | Cria um usuário                                   | `POST`      | ❌                       | `Público`                        |
| `/sessions`             | Login                                             | `POST`      | ❌                       | `Público`                        |
| `/refunds`              | Cria uma solicitação de reembolso                 | `POST`      | ✅                       | `employee`                       |
| `/refunds`              | Lista todos os reembolsos                         | `GET`       | ✅                       | `manager`                        |
| `/refunds/{id}`         | Lista detalhes de um reembolso pelo ID            | `GET`       | ✅                       | `manager`, `employee`            |
| `/uploads`              | Faz o upload de um comprovante                    | `POST`      | ✅                       | `employee`                        |
