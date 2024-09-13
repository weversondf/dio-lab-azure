# Desafio de projeto
Tutorial Desafio de projeto "Configurando uma instância de Banco de Dados na Azure" desenvolvido durante o Bootcamp Microsoft Azure Essentials na DIO

## Objetivo
Documentar um passo a passo para Configurar uma instância de Banco de Dados na Azure

## Tutorial Criando Máquinas Virtuais no Azure

Passo 1: **Acessar o Portal do Azure**  
+ Acesse o Portal do Azure e faça login com sua conta.  
+ No menu à esquerda, selecione "SQL databases".  

Passo 2: **Criar um Banco de Dados SQL**  
+ Clique em **+Create** para iniciar a criação de um novo banco de dados.  
+ Preencha as informações básicas:  
  - **Subscription**: Selecione sua assinatura do Azure.
  - **Resource group**: Escolha um grupo de recursos existente ou crie um novo.
  - **Database name**: Insira o nome do seu banco de dados.
  - **Server**: Crie um novo servidor ou selecione um existente.
+ Para criar um novo servidor, clique em **Create new**.
+ Insira um nome para o servidor.
+ Defina um nome de usuário e uma senha de administrador.
+ Escolha a localização do servidor.

Passo 3: **Configurar o Preço e o Desempenho**
+ Na seção **Compute + storage**, selecione a camada de preço e desempenho que melhor se adequa às suas necessidades.
+ Configure o tamanho do armazenamento e o número de DTUs (Database Transaction Units) ou vCores.

Passo 4: **Configurar a Rede**
+ Na seção **Networking**, configure as regras de firewall para permitir o acesso ao banco de dados a partir de endereços IP específicos ou redes virtuais.
+ Habilite ou desabilite o acesso público conforme necessário.

Passo 5: **Revisar e Criar**
+ Revise todas as configurações na seção **Review + create**.
+ Clique em Create para iniciar a implantação do banco de dados.

Passo 6: **Conectar ao Banco de Dados**
+ Após a criação, vá para a página do banco de dados no portal do Azure.
+ Anote o **Server name**.
+ Use o SQL Server Management Studio (SSMS) ou outra ferramenta de sua preferência para se conectar ao banco de dados usando o nome do servidor, o nome de usuário e a senha definidos anteriormente.

Passo 7: **Configurar o Banco de Dados**
+ No SSMS, conecte-se ao servidor SQL do Azure.
+ Crie tabelas, insira dados e execute consultas conforme necessário.

## Referências
- [Documentação oficial do Azure](https://learn.microsoft.com/pt-br/azure/azure-sql/managed-instance/instance-create-quickstart?view=azuresql)
- [Criar Instância Gerenciada de SQL do Azure](https://learn.microsoft.com/pt-br/azure/azure-sql/managed-instance/instance-create-quickstart?view=azuresql&tabs=azure-portal)
- [Como criar banco de dados Azure SQL](https://www.youtube.com/watch?v=ZNtRxoyV0z0)
- [Como INSTALAR e CONFIGURAR o SQL Server - O Guia Completo](https://www.youtube.com/watch?v=Lc3yclqM8rQ)

## Ferramentas
![Azure](https://img.shields.io/badge/azure-%230072C6.svg?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Windows 11](https://img.shields.io/badge/Windows%2011-%230079d5.svg?style=for-the-badge&logo=Windows%2011&logoColor=white)
![Microsoft SQL Server](https://img.shields.io/badge/Microsoft%20SQL%20Server-CC2927?style=for-the-badge&logo=microsoft%20sql%20server&logoColor=white)
[![GitHub](https://img.shields.io/badge/GitHub-000?style=for-the-badge&logo=github&logoColor=30A3DC)](https://docs.github.com/)
[![Git](https://img.shields.io/badge/Git-000?style=for-the-badge&logo=git&logoColor=E94D5F)](https://git-scm.com/doc)
