# Desafio de projeto
Tutorial do Desafio de projeto "Otimizando Custos no Azure" desenvolvido durante o Bootcamp Microsoft Azure Essentials na DIO

## Passo 1. Monitorar e Controlar Custos com Azure Cost Management

O **Azure Cost Management** oferece ferramentas para monitorar, controlar e otimizar os gastos.

- Acesse o **Azure Cost Management** no portal do Azure.
- Configure **alertas de orçamento**: Defina um limite de gastos e receba notificações quando você estiver se aproximando ou ultrapassando esse valor.
  - Vá até **Custos e Orçamentos** e crie um **novo orçamento**.
- Utilize o **Relatório de Custos** para analisar seus gastos por serviço, região e assinatura.
  - Identifique quais serviços estão gerando mais custos e ajuste conforme necessário.

## Passo 2. Escolher o Tamanho e Tipo de VM Correto

A escolha do tipo e tamanho correto de VM pode impactar significativamente seus custos.

- Ao criar uma VM, selecione uma que atenda às suas necessidades de CPU, memória e armazenamento sem excessos.
  - Considere utilizar **VMs de baixo custo**, como as séries B, que são ideais para cargas de trabalho que não precisam de desempenho constante.
- Habilite o **dimensionamento automático** (auto-scaling) para que a VM aumente ou diminua conforme a demanda, evitando o pagamento por recursos ociosos.
  - Acesse o **Conjunto de Dimensionamento de VMs** e configure o **escalonamento automático** com base em métricas como uso de CPU.

## Passo 3. Utilizar Instâncias Reservadas

As **instâncias reservadas** oferecem grandes descontos em VMs e outros serviços do Azure quando você se compromete com um contrato de longo prazo (1 ou 3 anos).

- Vá até **Reservas de Instâncias** no portal do Azure.
- Avalie o uso de suas VMs atuais e considere reservar instâncias que têm uso constante para obter descontos de até 72%.

## Passo 4. Gerenciar Armazenamento de Forma Eficiente

Armazenamento pode ser um grande gerador de custos, especialmente se não for bem gerenciado.

- Utilize **camadas de armazenamento** para otimizar o custo de acordo com a frequência de acesso:
  - **Hot**: Ideal para dados acessados com frequência.
  - **Cool**: Para dados acessados com pouca frequência.
  - **Archive**: Para dados que raramente são acessados e podem ser armazenados a longo prazo.
- Limpe dados não utilizados ou antigos regularmente e automatize a exclusão de blobs expirados com **Azure Blob Lifecycle Management**.
  - No portal do Azure, configure políticas de ciclo de vida para mover automaticamente dados entre camadas ou excluir após um período de tempo.

## Passo 5. Otimizar o Uso da Rede

O tráfego de rede também pode contribuir para os custos, especialmente se envolver grandes volumes de dados ou comunicações entre regiões diferentes.

- **Minimize o tráfego entre regiões**: Mantenha seus serviços na mesma região para evitar cobranças adicionais de transferência de dados.
- Utilize **Azure Front Door** ou **CDN** para otimizar a entrega de conteúdo, melhorando a performance e reduzindo custos de transferência de dados.

## Passo 6. Automatizar a Parada de VMs Não Utilizadas

VMs que continuam em execução, mesmo quando não são necessárias, podem gerar custos desnecessários.

- Configure **Runbooks** no **Azure Automation** para parar automaticamente VMs fora do horário de uso, como à noite ou em fins de semana.
  - No portal, acesse **Azure Automation**, crie um novo **Runbook** e defina um agendamento para desligar as VMs em horários ociosos.

## Passo 7. Revisar Periodicamente Seus Recursos

- Realize revisões regulares para identificar recursos que não estão sendo utilizados, como VMs, discos e redes inativos.
- Utilize o **Azure Advisor** para obter recomendações de boas práticas e identificar oportunidades de otimização de custos.
  - O **Azure Advisor** oferece dicas como a identificação de VMs subutilizadas, sugerindo ajustes de capacidade.

## Passo 8. Otimizar o Uso de Licenças

Se você está utilizando o **Windows Server** ou o **SQL Server**, certifique-se de aproveitar os **Benefícios Híbridos do Azure** para utilizar suas licenças existentes no Azure.

- Acesse o **Azure Hybrid Benefit** e aplique suas licenças existentes de software para reduzir custos.

## Passo 9. Consolidar Recursos com Gerenciamento de Grupos

Agrupe seus recursos para facilitar a visualização e o gerenciamento centralizado.

- Utilize **Grupos de Recursos** para organizar e gerenciar serviços relacionados.
  - No painel do Azure, crie um novo grupo de recursos e mova serviços relacionados para esse grupo, facilitando o acompanhamento de custos.

## Passo 10. Usar Serviços Serverless

Sempre que possível, opte por serviços **serverless**, como **Azure Functions** ou **Logic Apps**, onde você paga apenas pelo tempo de execução do código e pelos recursos consumidos durante a execução.

- Acesse o **Azure Functions** e crie uma nova **Função**.
  - Configure o acionador da função para ser executado apenas quando necessário, economizando recursos.

## Referências
- Conceitos básicos do Microsoft Azure: Descrever o gerenciamento e a governança do Azure
  - [Unidade 1 - Introdução](https://learn.microsoft.com/training/modules/describe-cost-management-azure/1-introduction)
  - [Unidade 2 - Descrever fatores que podem afetar os custos no Azure](https://learn.microsoft.com/training/modules/describe-cost-management-azure/2-describe-factors-affect-costs-azure )
  - [Unidade 3 - Comparar as calculadoras Preço e Custo Total de Propriedade](https://learn.microsoft.com/training/modules/describe-cost-management-azure/3-compare-pricing-total-cost-of-ownership-calculators )
  - [Unidade 6 - Descreva a ferramenta Gerenciamento de Custos da Microsoft](https://learn.microsoft.com/training/modules/describe-cost-management-azure/6-describe-azure-tool )
- [Tutorial: Otimizar os custos usando recomendações](https://learn.microsoft.com/pt-br/azure/cost-management-billing/costs/tutorial-acm-opt-recommendations)
