# Desafio de projeto
Tutorial do Desafio de projeto "Ferramentas de Implantação na Azure" desenvolvido durante o Bootcamp Microsoft Azure Essentials na DIO

## Passo 1. Acessando o Shell no Azure

O **Azure Cloud Shell** é uma ferramenta baseada em navegador que oferece um ambiente de linha de comando para gerenciar seus recursos no Azure. Você pode usar o Cloud Shell diretamente no portal do Azure, sem precisar instalar ferramentas localmente.

Para acessar o Azure Cloud Shell:

1. **Acesse o Portal do Azure**:
   - Faça login no [Portal do Azure](https://portal.azure.com/).

2. **Inicie o Cloud Shell**:
   - Clique no ícone de **Cloud Shell** no canto superior direito do portal, que se parece com um terminal.

3. **Escolha o Tipo de Shell**:
   - O Cloud Shell oferece suporte para **Bash** e **PowerShell**. Selecione o ambiente que melhor se adapta às suas necessidades.

4. **Use o Shell**:
   - Após iniciar o Shell, você pode executar comandos diretamente no navegador para gerenciar seus recursos Azure.

## Passo 2. Área de Automação no Azure

A **Área de Automação no Azure** é um conjunto de ferramentas e serviços que permite automatizar tarefas e processos de gerenciamento de recursos. Isso inclui:

- **Azure Automation**: Um serviço que oferece automação de tarefas recorrentes, gerenciamento de atualizações e configuração de ambientes.
- **Runbooks**: Scripts que automatizam tarefas administrativas, como o gerenciamento de atualizações e a automação de processos.
- **Azure Logic Apps**: Uma ferramenta para criar fluxos de trabalho automáticos entre aplicativos e serviços para integrar e automatizar processos de negócios.

Essas ferramentas ajudam a melhorar a eficiência e a consistência na administração de ambientes Azure, permitindo a criação de soluções personalizadas para suas necessidades.

## Passo 3. Azure Bicep

O **Azure Bicep** é uma linguagem de infraestrutura como código (IaC) que simplifica a criação e o gerenciamento de recursos Azure. É uma alternativa ao Azure Resource Manager (ARM) templates, oferecendo uma sintaxe mais simples e legível.

### Características do Azure Bicep:
- **Sintaxe Simples**: Reduz a complexidade dos templates ARM com uma sintaxe mais amigável.
- **Integração com o Azure**: Funciona diretamente com o Azure Resource Manager para provisionar e gerenciar recursos.
- **Modularidade**: Permite a criação de módulos reutilizáveis para simplificar a definição de recursos.

Para começar com Azure Bicep, você pode escrever arquivos `.bicep` e implantá-los usando o Azure CLI ou o Azure PowerShell.

    ```bicep
    param location string - resourceGroup().location
    param storageAccountName string = 'toylaunch${uniqueString(resourceGroup().id)}
    
    resource storageAccount 'Microsoft.Storage/storageAccounts@2021-06-01' = {
    name: storageAccountName
    location: location
    sku: {
    name: 'Standard_LRS'
    
    kind: 'StorageV2'
    properties: {
    accessTier: 'Hot'
    ```

## Passo 4. Azure Arc

O **Azure Arc** é uma solução que estende os serviços do Azure para ambientes locais e outras nuvens, permitindo que você gerencie recursos híbridos e multi-nuvem como se estivessem no Azure.

### Principais Recursos do Azure Arc:
- **Gerenciamento Centralizado**: Oferece uma visão unificada para gerenciar recursos em ambientes locais, em outras nuvens e no Azure.
- **Aplicações e Kubernetes**: Permite a implantação e a gestão de aplicativos em Kubernetes, seja no Azure ou fora dele.
- **Políticas e Segurança**: Aplica políticas e controles de segurança consistentes em todos os seus recursos, independentemente de onde eles estejam.

O Azure Arc proporciona flexibilidade e controle adicional, ajudando a criar uma experiência híbrida e multi-nuvem coesa.

## Referências
- Conceitos básicos do Microsoft Azure: Descrever o gerenciamento e a governança do Azure / Descrever recursos e ferramentas para gerenciar e implantar recursos do Azure 
   - [Unidade 1 - Introdução](https://learn.microsoft.com/training/modules/describe-features-tools-manage-deploy-azure-resources/1-introduction)
   - [Unidade 3 - Descrever a finalidade do Azure Arc](https://learn.microsoft.com/training/modules/describe-features-tools-manage-deploy-azure-resources/3-describe-purpose-of-azure-arc)
- [O que é infraestrutura como código (IaC)?](https://learn.microsoft.com/en-us/devops/deliver/what-is-infrastructure-as-code#deploy-iac-on-azure)
- [Como inventariar seu ambiente Azure](https://www.youtube.com/watch?v=vKk7E26b1e8)
- [Azure Bicep Repo GitHub Examples](https://github.com/Azure/bicep/tree/main)
- [Entender a estrutura e a sintaxe dos arquivos Bicep](https://learn.microsoft.com/pt-br/azure/azure-resource-manager/bicep/file)
