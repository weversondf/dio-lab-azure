# Desafio de projeto
Tutorial Desafio de projeto "Criando máquinas Virtuais na Azure" desenvolvido durante o Bootcamp Microsoft Azure Essentials

## Objetivo
Documentar um passo a passo para Criando máquinas Virtuais na Microsoft Azure

## Tutorial Criando Máquinas Virtuais no Azure
Passo 1: **Acesse o Portal do Azure**: Primeiro, faça login no Portal do Azure com sua conta.

Passo 2: **Crie uma Máquina Virtual**:
* Na barra de pesquisa, digite “máquinas virtuais” e selecione “Máquinas virtuais” nos resultados.
* Clique em “Adicionar” e escolha “Máquina virtual do Azure”.
* Preencha os detalhes da instância:
	* Nome da máquina virtual (por exemplo, “minhaVM”).
	* Escolha a imagem (Windows Server, Linux etc.).
	* Configure a conta de administrador com nome de usuário e senha.
	* Defina as regras de porta de entrada (geralmente RDP e HTTP).
* Clique em “Revisar + criar” e, em seguida, em “Criar”.

Passo 3: **Conecte-se à Máquina Virtual**:
* Na página de visão geral da sua máquina virtual, clique em “Conectar” > “RDP”.
* Baixe o arquivo RDP (Remote Desktop Protocol).
* Abra o arquivo RDP e clique em “Conectar” quando solicitado.
* Insira o nome de usuário (geralmente “localhost\usuariodoazure”) e a senha criada para a máquina virtual.

Passo 4: **Personalize sua Máquina Virtual**:
Agora que você está conectado na máquina virtual, instale os softwares e configure as opções conforme necessário.

## Referências
- [Criar uma máquina virtual do Windows no portal do Azure](https://learn.microsoft.com/pt-pt/azure/virtual-machines/windows/quick-create-portal)
- [Criar uma máquina virtual do Windows no Azure](https://learn.microsoft.com/pt-br/training/modules/create-windows-virtual-machine-in-azure/)
- [Como usar a Área de Trabalho Remota no Windows 11 ou 10](https://support.microsoft.com/pt-br/windows/como-usar-a-%C3%A1rea-de-trabalho-remota-5fe128d5-8fb1-7a23-3b8a-41e636865e8c)
- [Criando Máquinas Virtuais usando o Azure CLI](https://www.youtube.com/watch?v=QymA3SWvJ0o)

## Ferramentas
![Azure](https://img.shields.io/badge/azure-%230072C6.svg?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Windows 11](https://img.shields.io/badge/Windows%2011-%230079d5.svg?style=for-the-badge&logo=Windows%2011&logoColor=white)
[![GitHub](https://img.shields.io/badge/GitHub-000?style=for-the-badge&logo=github&logoColor=30A3DC)](https://docs.github.com/)
[![Git](https://img.shields.io/badge/Git-000?style=for-the-badge&logo=git&logoColor=E94D5F)](https://git-scm.com/doc)
