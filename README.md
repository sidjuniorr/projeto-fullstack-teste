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


