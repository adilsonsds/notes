# Comando new

- `dotnet new list` -> Lista os templates
- `dotnet new <TEMPLATE>` -> Cria um projeto baseado num template (Ex: console, webapi, worker, xunit, angular)
- `dotnet new console -n NomeDoProjeto -o NomeDoDiretorio` -> Cria um projeto console

# Comando build

- `dotnet build` -> Faz build do projeto

# Comando run

- `dotnet run` -> Executa o projeto
- `dotnet run --project MeuProjeto/MeuProjeto.csproj` -> Executa o projeto
- `dotnet run --launch-profile Homologation` -> Executa o projeto com um profile específico

# Comando watch

- `dotnet watch <COMMAND>` -> Hot reload. Usado em conjunto com comandos como `run`, `test`, `build`
- `dotnet watch run` -> Executa o projeto e fica observando alteracões

# Comando sln

- `dotnet new sln -n NomeDaSolution` -> Cria uma solution
- `dotnet sln MinhaSolution.sln list` -> Lista os projetos da solution
- `dotnet sln MinhaSolution.sln add MeuProjeto/MeuProjeto.csproj` -> Adiciona um projeto na solution
- `dotnet sln MinhaSolution.sln add Frontend/Frontend.csproj Backend/Backend.csproj` -> Adiciona múltiplos projetos na solution
- `dotnet sln todo.sln add **/*.csproj` -> Adiciona múltiplos projetos na solution usando pattern (Unix olny)
- `dotnet sln todo.sln add (ls -r **/*.csproj)` -> Adiciona múltiplos projetos na solution usando pattern (Powershell)
- `dotnet sln MinhaSolution.sln remove MeuProjeto/MeuProjeto.csproj` -> Remove um projeto na solution

# Comando add/remove/list reference

- `dotnet add Prjeto1.csproj reference Projeto2.csproj` -> Adiciona uma referência
- `dotnet add Prjeto1.csproj reference Projeto2.csproj Projeto3.csproj` -> Adiciona múltiplas referências
- `dotnet add Prjeto1.csproj reference **/*.csproj` -> Adiciona múltiplas referências usando pattern (Unix)
- `dotnet remove Prjeto1.csproj reference Projeto2.csproj` -> Remove uma referência
- `dotnet list Prjeto1.csproj reference` -> Lista as referências

# Git ignore

- `dotnet new gitignore` -> Gera um arquivo .gitignore para projetos dotnet

# Comando add package

- `dotnet add package <PACKAGE_NAME>` -> Instala um pacote nuget
- `dotnet add package Newtonsoft.Json --version 12.0.1` -> Instala um pacoter nuget com uma versão específica

# Docker

## Entrypoints

- `ENTRYPOINT ["dotnet", "MyProject.dll"]` -> Define o entrypoint do dockerfile
- `ENTRYPOINT ["dotnet", "MyProject.dll", "--launch-profile Production"]` -> Define o entrypoint do dockerfile e executa o app com um profile específico

# AWS

## Lambda Templates

- `dotnet tool install -g Amazon.Lambda.Tools` -> Instala e/ou atualiza ferramentas para AWS Lambda
- `dotnet new -i Amazon.Lambda.Templates` -> Instala os templates para AWS Lambda
- `dotnet new lambda.EmptyFunction -n MyProjectName` -> Cria um projeto .NET usando template para AWS Lambda 