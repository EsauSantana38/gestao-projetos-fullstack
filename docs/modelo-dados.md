# Modelo de Dados Relacional

Este documento descreve o modelo de dados utilizado
no sistema de gestão de projetos, tarefas e usuários.

O banco de dados foi modelado para permitir o controle
de projetos, suas tarefas e os usuários envolvidos.

---

## Entidades Principais

### Usuario
Representa os usuários do sistema.

Campos:
- id_usuario (PK)
- nome
- email
- senha
- data_nascimento
- status

---

### Projeto
Representa um projeto que agrupa várias tarefas.

Campos:
- id_projeto (PK)
- nome
- descricao
- data_inicio
- data_conclusao
- status
- responsavel

---

### Tarefa
Representa uma tarefa ou atividade de um projeto.

Campos:
- id_tarefa (PK)
- titulo
- descricao
- data_criacao
- data_conclusao
- prioridade
- status
- id_projeto (FK)

---

## Relacionamentos

- Um Projeto possui várias Tarefas (1:N)
- Um Usuário pode participar de várias Tarefas (N:N)
- Uma Tarefa pode ter vários Usuários associados
