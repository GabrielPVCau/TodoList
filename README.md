# To-do List em Python

O projeto é uma lista de tarefas que permite ao usuário adicionar e visualizar tarefas. Ele se integra com uma API criada no Supabase, uma plataforma de desenvolvimento de aplicativos, para armazenar e gerenciar as informações das tarefas. A interface do usuário é construída com a biblioteca Tkinter do Python.

## Funcionalidades

- Adicionar tarefas
- Recuperar lista de tarefas
## Screenshots

![App Screenshot](https://raw.githubusercontent.com/welyson1/TodoList/493108bba3ba5b50f7db7abe70cd2ed95a657f24/img/Tela.png)

## Instalação banco de dados offline
1. Execute o comando abaixo no terminal
```bash
  pip install psycopg2
```

2. Instale o PgAdmin

3. Crie um banco de dados e a tabela com a query abaixo

```SQL
  CREATE TABLE todo_list (
    id SERIAL PRIMARY KEY,
    task_name VARCHAR(255) NOT NULL,
    due_date DATE,
    priority INT,
    completed BOOLEAN DEFAULT false
  );
```

## Instalação banco de dados online
1. Crie uma conta no Supabase em https://supabase.com/

2. Crie um projeto

3. Use o SQL Editor para criar a tabela
```SQL
  CREATE TABLE todo_list (
    id SERIAL PRIMARY KEY,
    task_name VARCHAR(255) NOT NULL,
    due_date DATE,
    priority INT,
    completed BOOLEAN DEFAULT false
  );
```

4. Pegue as credenciais em Project Settings > Database

5. Preencha a função abaixo com as credenciais
```Python
self.conn = psycopg2.connect(
  # Coloque as credenciais do banco de dados postgres aqui
  host="host",
  database="postgres",
  user="postgres",
  password="senha"
)
```
    
## License

[MIT](https://choosealicense.com/licenses/mit/)

