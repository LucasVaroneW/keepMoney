# keepMoney
Instalar sequelize-cli como una dependencia de desarrollo en tu proyecto:
css
Copy code
npm install --save-dev sequelize-cli
Configurar un archivo config.json en la raíz de tu proyecto con los detalles de tu base de datos, tal como lo hicimos anteriormente:
json
Copy code
{
  "development": {
    "username": "root",
    "password": "root",
    "database": "mydatabase",
    "host": "localhost",
    "dialect": "mysql"
  }
}
Inicializar el proyecto de sequelize-cli en tu directorio raíz:
csharp
Copy code
npx sequelize-cli init
Crear la base de datos utilizando sequelize-cli:
lua
Copy code
npx sequelize-cli db:create
Crear los modelos de Sequelize (con los campos que deseas) utilizando sequelize-cli:
go
Copy code
npx sequelize-cli model:generate --name User --attributes username:string, fullName:string, email:string, password:string
Ejecutar la migración para crear la tabla de usuarios en la base de datos:
Copy code
npx sequelize-cli db:migrate
