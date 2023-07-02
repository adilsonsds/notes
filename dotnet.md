# Comandos new

- `dotnet new list` -> Lista os templates
- `dotnet new <TEMPLATE>` -> Cria um projeto baseado num template (Ex: console, webapi, worker, xunit, angular)
- `dotnet new console -n NomeDoProjeto -o NomeDoDiretorio` -> Cria um projeto console


# Comandos build

- `dotnet build` -> Faz build do projeto

# Comandos run

- `dotnet run` -> Executa o projeto

# Comandos watch

- `dotnet watch <COMMAND>` -> É usado em conjunto com comandos como `run`, `test`, `build` para monitorar arquivos em busca de alteracões e atualizar automaticamente (hot reload).
- `dotnet watch run` -> Executa o projeto e fica observando alteracões.