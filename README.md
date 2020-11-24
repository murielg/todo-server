# todo-server
Ktor Server for Todo's App

## Local Environment Setup
- Install postgres `brew install postgresql` 
- Create a database named **todos** :

```
psql -U postgres
create database todos;
```

- In IntelliJ: 
  - Add a new Kotlin configuration named Server
  - Choose `todoserver.main` under **use classpath of module**
  - Select **ApplicationKt** in the **Main class** field
  - Under **Environment Variables** add the following variables

```
  JDBC_DRIVER=org.postgresql.Driver
  JDBC_DATABASE_URL=jdbc:postgresql:todos?user=postgres
  SECRET_KEY=YOURSECRETKEYHERE
  JWT_SECRET=YOURJWTSECRETKEYHERE
```

