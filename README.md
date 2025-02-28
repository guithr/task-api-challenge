# 📌 Desafio prático -API de Gerenciamento de Tasks

## 🔥 Funcionalidades

✅ Criar uma nova task <br>
✅ Listar todas as tasks <br>
✅ Atualizar uma task pelo `id` <br> 
✅ Remover uma task pelo `id` <br>
✅ Marcar uma task como completa <br>
✅ Importação de tasks via CSV <br>

---

## 📌 Estrutura da Task

Cada task contém as seguintes propriedades:

```json
{
  "id": "uuid",
  "title": "Título da task",
  "description": "Descrição da task",
  "completed_at": null,
  "created_at": "2025-02-28T12:00:00.000Z",
  "updated_at": "2025-02-28T12:00:00.000Z"
}
```

---

## 🚀 Rotas e Regras de Negócio

### 🔹 Criar uma Task
📌 **POST - /tasks**

Cria uma task utilizando `title` e `description`.

### 🔹 Listar todas as Tasks
📌 **GET - /tasks**

Retorna todas as tasks salvas no banco de dados com suporte a filtros por `title` e `description`.

### 🔹 Atualizar uma Task
📌 **PUT - /tasks/:id**

Atualiza `title` e/ou `description` de uma task existente.

### 🔹 Remover uma Task
📌 **DELETE - /tasks/:id**

Exclui uma task após validação de existência.

### 🔹 Marcar uma Task como Completa
📌 **PATCH - /tasks/:id/complete**

Alterna o status de conclusão da task.

### 🔹 Importação de Tasks via CSV
Permite importar tasks em massa a partir de um arquivo CSV.

📂 **Exemplo de Estrutura CSV:**
```csv
  title,description
  "Tarefa 1","Descrição da tarefa 1"
  "Tarefa 2","Descrição da tarefa 2"
```

📌 **Para importar o CSV, utilize o seguinte comando:**
```sh
node src/streams/task.csv
```

---

## ⚡ Como Executar o Projeto

1️⃣ Clone o repositório
   ```sh
   git clone https://github.com/guithr/task-api-challenge.git
   ```
2️⃣ Instale as dependências
   ```sh
   npm install
   ```
3️⃣ Execute o servidor
   ```sh
   npm run dev
   ```

---

## 🛠 Tecnologias Utilizadas

- **Node.js**
- **Express**
- **CSV Parsing Library**
- **Banco de Dados Local (JSON)**

---

## 🚀 Desafio da Rocketseat  

Este projeto foi desenvolvido como parte do **Desafio 01** da trilha **Node.js** do programa **Ignite** da Rocketseat.  

🔗 **Link do Desafio:** [Desafio 01 - API](https://efficient-sloth-d85.notion.site/Desafio-01-2d48608f47644519a408b438b52d913f#2943738b73d14873b67270c2ef93cf4b)  

O objetivo do desafio é construir uma API para gerenciar tarefas (*tasks*), aplicando conceitos como:  
✅ Manipulação de requisições HTTP sem frameworks externos  
✅ Persistência de dados com um banco de dados local baseado em JSON  
✅ Processamento de arquivos CSV utilizando Streams  
✅ Implementação de CRUD completo  

---

