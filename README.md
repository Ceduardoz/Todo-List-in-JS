# 📝 To-Do List em React

Aplicação de lista de tarefas (To-Do List) desenvolvida com **React** e **JavaScript**, com persistência de dados utilizando **Local Storage** do navegador.

---

## 📌 Sobre o Projeto

Este projeto consiste em uma aplicação simples e funcional para gerenciamento de tarefas, permitindo que o usuário:

- ✅ Adicione novas tarefas
- ✏️ Edite tarefas existentes
- ✔️ Marque tarefas como concluídas
- 🗑️ Remova tarefas
- 💾 Tenha suas tarefas salvas automaticamente no **Local Storage**

O principal objetivo do projeto é praticar conceitos fundamentais do React como:

- Componentização
- Hooks (`useState`, `useEffect`)
- Manipulação de eventos
- Renderização condicional
- Persistência de dados no navegador

---

## 🚀 Tecnologias Utilizadas

- ⚛️ React
- 🟨 JavaScript (ES6+)
- 🎨 CSS3
- 🌐 Local Storage API

---

## 🧠 Funcionalidades

### ➕ Adicionar Tarefa
O usuário pode digitar uma tarefa e adicioná-la à lista.

### ✔️ Marcar como Concluída
Ao clicar na tarefa, ela pode ser marcada como concluída (com alteração visual).

### ✏️ Editar Tarefa
Permite atualizar o texto da tarefa.

### 🗑️ Remover Tarefa
Remove permanentemente a tarefa da lista.

### 💾 Persistência com Local Storage
As tarefas são armazenadas no navegador usando `localStorage`, garantindo que os dados permaneçam salvos mesmo após atualizar ou fechar a página.

---

## 💾 Como Funciona o Local Storage

A aplicação utiliza o hook `useEffect` para:

- 🔄 Carregar as tarefas salvas ao iniciar a aplicação
- 💾 Salvar automaticamente sempre que houver alteração na lista

```javascript
// Carregar tarefas ao iniciar
useEffect(() => {
  const storedTasks = localStorage.getItem("tasks");
  if (storedTasks) {
    setTasks(JSON.parse(storedTasks));
  }
}, []);

// Salvar tarefas sempre que houver alteração
useEffect(() => {
  localStorage.setItem("tasks", JSON.stringify(tasks));
}, [tasks]);
