# Desafio de projeto
Tutorial do Desafio de projeto "Dominando o Armazenamento na Azure" desenvolvido durante o Bootcamp Microsoft Azure Essentials na DIO

## Passo 1. Acessar o Portal do Azure

Primeiro, faça login no [Portal do Azure](https://portal.azure.com). O portal oferece uma interface visual para gerenciar todos os seus recursos de armazenamento.

## Passo 2. Criar uma Conta de Armazenamento

- No painel do Azure, vá até **Criar Recurso**.
- Pesquise por **Conta de Armazenamento** e clique em **Criar**.
- Preencha os seguintes detalhes:
  - **Assinatura**: Selecione a assinatura adequada.
  - **Grupo de Recursos**: Escolha um grupo existente ou crie um novo.
  - **Nome da Conta de Armazenamento**: Insira um nome único.
  - **Região**: Selecione a região onde os dados serão armazenados, levando em conta a proximidade dos usuários e a latência.
  - **Desempenho**: Escolha entre **Standard** (disco rígido) ou **Premium** (SSD), dependendo das suas necessidades de desempenho.
  - **Redundância**: Defina o nível de replicação dos dados:
    - **LRS (Local-Redundant Storage)**: Armazena cópias dos dados dentro de um único datacenter.
    - **GRS (Geo-Redundant Storage)**: Replica os dados para uma região secundária, garantindo mais segurança em casos de desastres.
    - **ZRS (Zone-Redundant Storage)**: Replica os dados entre zonas dentro de uma mesma região.

## Passo 3. Configurar o Armazenamento Blob

O Blob Storage é utilizado para armazenar grandes quantidades de dados não estruturados, como arquivos, imagens e vídeos.

- Após criar a Conta de Armazenamento, acesse **Serviços de Armazenamento** no painel da conta.
- Selecione **Containers** e clique em **Adicionar** para criar um novo container.
- Escolha o nível de acesso:
  - **Privado**: Apenas o proprietário tem acesso.
  - **Público (somente leitura)**: Qualquer pessoa pode visualizar os dados, mas não modificá-los.
- Após criar o container, você pode **carregar** arquivos diretamente ou usar o **Azure CLI** ou **Azure Storage Explorer** para gerenciar dados.

## Passo 4. Utilizar o Armazenamento de Arquivos

O **Azure Files** oferece um sistema de arquivos compartilhado que pode ser montado em VMs ou acessado via protocolo SMB (Server Message Block).

- No painel da Conta de Armazenamento, clique em **File Shares**.
- Selecione **Adicionar** para criar um novo compartilhamento de arquivos.
- Defina o **Nome do Compartilhamento** e o **tamanho máximo** em GB.
- Após a criação, você pode montar o compartilhamento de arquivos em uma máquina virtual ou servidor usando os comandos fornecidos na aba de conexão.

## Passo 5. Armazenamento de Tabelas

O **Azure Table Storage** é um serviço NoSQL que permite o armazenamento de grandes volumes de dados semi-estruturados.

- No painel da Conta de Armazenamento, clique em **Tabelas**.
- Selecione **Adicionar** e defina um nome para a tabela.
- Utilize o **Azure SDK**, **API REST** ou **Azure Storage Explorer** para adicionar, consultar ou excluir dados na tabela.

## Passo 6. Armazenamento de Filas

O **Azure Queue Storage** é ideal para o gerenciamento de mensagens entre componentes distribuídos, oferecendo uma maneira simples de comunicação assíncrona.

- No painel da Conta de Armazenamento, clique em **Filas**.
- Selecione **Adicionar** para criar uma nova fila.
- Dê um nome à fila e configure as permissões de acesso.
- Você pode enviar e receber mensagens através da **API REST** ou usando o **SDK do Azure** para .NET, Python, Java ou outras linguagens.

## Passo 7. Configurar Políticas de Acesso e Segurança

- No painel da Conta de Armazenamento, acesse a aba de **Chaves de Acesso**. Essas chaves permitem que você autentique programaticamente suas operações de armazenamento.
- Alternativamente, configure **SAS (Shared Access Signatures)** para fornecer acesso temporário e controlado a recursos específicos.
- Habilite a **Criptografia no Armazenamento** para garantir que os dados sejam criptografados em repouso.

## Passo 8. Gerenciar Backups e Replicação

- Para garantir a recuperação de dados em caso de falhas, configure o **Azure Backup**.
- Habilite a **Geo-Redundância** para garantir que seus dados estejam replicados em uma região secundária.
- Monitore o status da replicação e gerencie cópias usando o painel da Conta de Armazenamento.

## Passo 9. Monitoramento e Alertas

- Utilize o **Azure Monitor** para acompanhar o uso e desempenho do armazenamento.
- Configure **alertas** para ser notificado quando os limites de capacidade forem atingidos ou quando houver falhas de operação.

## Passo 10. Dimensionar Armazenamento

- Se o uso de armazenamento aumentar, você pode ajustar o **tamanho do armazenamento** e adicionar novas contas de armazenamento conforme necessário.
- Utilize a opção de **Dimensionamento Automático** para ajustar o desempenho e a capacidade de forma dinâmica, garantindo alta disponibilidade e desempenho adequado.

## Referências - Descrever as contas de armazenamento do Azure
- [Unidade 2 de 9](https://learn.microsoft.com/training/modules/describe-azure-storage-services/2-accounts)
- [Unidade 3 de 9](https://learn.microsoft.com/training/modules/describe-azure-storage-services/3-redundancy)
- [Unidade 4 de 9](https://learn.microsoft.com/training/modules/describe-azure-storage-services/4-describe-azure-storage-services)
- [Unidade 6 de 9](https://learn.microsoft.com/training/modules/describe-azure-storage-services/6-identify-azure-data-migration-options)
- [AULA Armazenamento de dados com Azure Blob Storage na prática](https://www.youtube.com/watch?v=OfqbRcPugUg)
