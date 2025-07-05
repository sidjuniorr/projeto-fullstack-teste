# Projeto Fullstack de Gerenciamento de Tarefas

Este é um projeto fullstack simples para gerenciar tarefas, desenvolvido com Flask para o backend e Vue.js para o frontend.

## Estrutura do Projeto

```
projeto-fullstack/
├── backend/        # Backend em Flask
│   ├── src/
│   │   └── main.py # Arquivo principal da API
│   ├── requirements.txt
│   └── venv/       # Ambiente virtual Python
└── frontend/       # Frontend em Vue.js
    ├── src/
    │   ├── App.vue # Componente principal
    │   └── main.js # Arquivo de entrada
    ├── package.json
    └── node_modules/
```

## Funcionalidades

- ✅ Adicionar novas tarefas
- ✅ Listar todas as tarefas
- ✅ Marcar tarefas como concluídas/não concluídas
- ✅ Excluir tarefas
- ✅ Interface responsiva

## Como Rodar o Projeto

### Backend (Flask)

1. Navegue até a pasta do backend:
   ```bash
   cd backend
   ```

2. Ative o ambiente virtual:
   ```bash
   source venv/bin/activate  # Linux/Mac
   # ou
   venv\Scripts\activate     # Windows
   ```

3. Execute o servidor:
   ```bash
   python src/main.py
   ```

O backend estará rodando em `http://localhost:5000`

### Frontend (Vue.js)

1. Em outro terminal, navegue até a pasta do frontend:
   ```bash
   cd frontend
   ```

2. Execute o servidor de desenvolvimento:
   ```bash
   npm run dev
   ```

O frontend estará rodando em `http://localhost:3000`

## API Endpoints

- `GET /` - Mensagem de boas-vindas
- `GET /tarefas` - Lista todas as tarefas
- `POST /tarefas` - Cria uma nova tarefa
- `PUT /tarefas/<id>` - Atualiza uma tarefa existente
- `DELETE /tarefas/<id>` - Exclui uma tarefa

## Tecnologias Utilizadas

### Backend
- Flask 2.3.2
- Flask-CORS 3.0.10

### Frontend
- Vue.js 3.3.4
- Axios 1.4.0
- Vite 4.4.5

## Como Rodar o Projeto com Docker

Certifique-se de ter o Docker e o Docker Compose instalados em sua máquina.

1.  Navegue até a raiz do projeto (`projeto-fullstack`):
    ```bash
    cd projeto-fullstack
    ```

2.  Construa as imagens Docker:
    ```bash
    docker compose build
    ```

3.  Inicie os contêineres:
    ```bash
    docker compose up -d
    ```

4.  Acesse o frontend em seu navegador: `http://localhost:8080`

5.  Para parar e remover os contêineres:
    ```bash
    docker compose down
    ```

## Integração Contínua (CI/CD) com GitHub Actions

Este projeto utiliza GitHub Actions para automatizar o processo de CI/CD. Em cada `push` ou `pull_request` para a branch `master`, o workflow irá:

1.  Executar os testes de backend (Pytest).
2.  Executar os testes de frontend (Vitest).
3.  Construir e enviar as imagens Docker do backend e frontend para o Docker Hub.

Você pode acompanhar o status das execuções na aba "Actions" do seu repositório GitHub.

As imagens Docker serão enviadas para o Docker Hub com as seguintes tags (substitua `seu-usuario-dockerhub` pelo seu nome de usuário):

*   `seu-usuario-dockerhub/fullstack-backend:<github_sha>`
*   `seu-usuario-dockerhub/fullstack-frontend:<github_sha>`
