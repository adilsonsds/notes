# Executar em container

Docker Hub - https://hub.docker.com/_/microsoft-mssql-server


```bash
docker run --name sqlserver -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=C0FL6d6RE#" -p 1433:1433 -d mcr.microsoft.com/mssql/server
```

Caso esteja usando WSL 2 no Windows, é preciso especificar o volume.

```bash
docker run -v ~/docker --name sqlserver -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=C0FL6d6RE#" -p 1433:1433 -d mcr.microsoft.com/mssql/server
```

### Connection String

```
Server=localhost,1433;Database=balta;User ID=sa;Password=C0FL6d6RE#;
```

### Erro de timeout ao conectar no SQL Server Management Studio

#### Solução 1

* Desligar VPN
* Reiniciar WSL

#### Solução 2

Obter o IP do WSL2 no terminal e trocar localhost pelo IP.

```
hostname -I
```

### Erro de SSL Provider

1. Reinstalar certificado
```
dotnet dev-certs https --clean
dotnet dev-certs https --trust
```

2. Atualizar connection string
```
Server=localhost,1433;Database=balta;User ID=sa;Password=C0FL6d6RE#;Trusted_Connection=False; TrustServerCertificate=True;
```

