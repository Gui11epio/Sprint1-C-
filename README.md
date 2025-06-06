# Sprint1- C#

## 📌 Descrição do Projeto

Este projeto consiste em uma API RESTful desenvolvida com ASP.NET Core, tenta representar uma solução de monitoramento de motos por meio de Rfid, com objetivo de gerenciar entidades como Motos, Filiais e Pátios. A aplicação implementa operações básicas de CRUD (Create, Read, Update, Delete) e segue uma arquitetura em camadas (Controllers, Application, Domain, Infrastructure). A TagRfid é criada automaticamente quando uma moto é cadastrada

## 👥 Nome e RM dos Integrantes

- Guilherme Camasmie Laiber de Jesus – RM554894

- Fernando Fernandes Prado – RM557982

- Pedro Manzo Yokoo – RM556115

## 🚀 Rotas Disponíveis

### 📍 MotoController - `/api/Moto`
- `GET /api/Moto`  
  Retorna todas as motos cadastradas.

- `GET /api/Moto/placa`  
  Retorna uma moto específica pela placa.

- `GET /api/Moto/pagina`  
  Retorna motos por meio de páginas.

- `POST /api/Moto`  
  Cria uma nova moto. Requer um corpo com os dados da moto.

- `PUT /api/Moto/placa`  
  Atualiza os dados de uma moto pela placa.

- `DELETE /api/Moto/placa`  
  Deleta os dados de uma moto pela placa.

> Os outros controllers (`FilialController`, `PatioController`) seguem estrutura semelhante com operações básicas de CRUD.

## 🛠️ Tecnologias Utilizadas

- [.NET 6 / ASP.NET Core](https://dotnet.microsoft.com/)
- C#
- Entity Framework Core
- Swagger (OpenAPI) para documentação
- Visual Studio 2022
- Oracle DataBase
- AutoMapper
- Migrations
- DataAnnotations

## ▶️ Instruções de Execução

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/Gui11epio/Sprint1-C-.git
   

2. **Vá até "lauchSettings.json"**
   
   ![image](https://github.com/user-attachments/assets/adaf4e75-7381-4550-9252-163149c1f16c)

3. **Coloque suas informações do Banco de Dados Oracle**

   ![image](https://github.com/user-attachments/assets/70c5914a-b683-406a-ac77-849e88a52bc9)

4. **Abra a terminal no projeto e coloque as mesmas informações do Oracle**
   ```bash
   $env:DEFAULT_CONNECTION = "User Id=xxxxxxx;Password=xxxxxx;Data Source=xxxxxxxxxxxx:1521/ORCL"

5. **Ainda na terminal, rode este comando para criar as tabelas em seu banco de dados:**
   ```bash
   dotnet ef database update

6. **Após tudo isso, rode o programa e o Swagger abrirá sozinho**
   ```bash
   https://localhost:7117/swagger


## 📬JSON de Teste

- Filial:
  
```bash
{
  "nome": "Filial Centro-SP",
  "cidade": "São Paulo",
  "pais": "Brasil"
}
```

- Pátio:
  
```bash
{
  "nome": "Pátio A1",
  "largura": "50.0",
  "comprimento": "120.0",
  "filialId": 1
}
```
ℹ️ Observação: largura e comprimento devem ser strings representando valores numéricos válidos (entre 5 e 500 para largura; entre 5 e 1000 para comprimento).


- Moto
  
```bash
{
  "placa": "ABC1D23",
  "modelo": "POP",
  "marca": "Yamaha",
  "status": "MANUTENCAO",
  "patioId": 1
}
```
🔤 A placa da Moto deve ser única, não deve repetir

🔤 Modelo e Status devem conter valores válidos dos enums MotoModelo e MotoStatus, como:

- MotoModelo: "POP", "SPORT", "ELETRICA"
  
- MotoStatus: "LIGADO", "DESLIGADO", "MANUTENCAO", "DISPONIVEL"

  



   
