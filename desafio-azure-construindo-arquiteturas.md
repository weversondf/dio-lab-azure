# Desafio de projeto
Tutorial do Desafio de projeto "Construindo Arquiteturas no Azure" desenvolvido durante o Bootcamp Microsoft Azure Essentials na DIO

## Passo 1: **Planejar a Arquitetura**

Antes de começar a construir no Azure, é essencial planejar a arquitetura da solução. Alguns pontos importantes incluem:
- Quais serviços do Azure serão utilizados? 
- Como os componentes se comunicarão entre si?
- Haverá necessidade de alta disponibilidade e escalabilidade?
- Quais são os requisitos de segurança e conformidade?

Definida a infraestrutura que sua aplicação precisa e considere usar na arquitetura no Azure, o Azure Well-Architected Framework, que oferece orientação e práticas recomendadas para melhorar a qualidade das arquiteturas. 
O framework é composto por cinco pilares: Confiabilidade, Segurança, Otimização de Custos, Excelência Operacional, Eficiência de Desempenho.

## Passo 2. **Criar um Grupo de Recursos**

- No Portal do Azure, pesquise por **Grupos de Recursos**.
- Clique em **Criar Grupo de Recursos**.
- Escolha a **assinatura** e dê um nome significativo ao grupo de recursos.
- Selecione a **região** onde deseja hospedar seus recursos.
- Finalize clicando em **Criar**.

Este grupo de recursos ajudará a organizar todos os recursos de infraestrutura, facilitando a gestão e o monitoramento.

## Passo 3: **Criar Rede Virtual (VNet)**

- No Portal do Azure, procure por **Redes Virtuais**.
- Clique em **Criar** e defina o nome da VNet.
- Escolha o **endereço IP** do espaço, que será usado para definir sub-redes e comunicação interna.
- Defina uma **sub-rede** inicial, garantindo que todos os serviços internos estejam conectados.
- Conclua criando a rede virtual.

## Passo 4: **Configurar Regras de Segurança**

- Crie **Grupos de Segurança de Rede (NSGs)** para controlar o tráfego de entrada e saída da sua rede.
- Defina regras para permitir o tráfego HTTP/HTTPS, portas específicas ou restrições de IP.
- Associe os NSGs à sua VNet e sub-redes conforme necessário.

## Passo 5: **Provisionar Máquinas Virtuais**

- No painel do Azure, pesquise por **Máquinas Virtuais** e clique em **Criar**.
- Escolha o **sistema operacional** e o **tamanho da máquina** com base nas necessidades da aplicação.
- Associe a máquina virtual à **rede virtual** criada anteriormente.
- Configure **nome de usuário e senha** para acesso remoto via SSH (para Linux) ou RDP (para Windows).
- Defina as **regras de acesso**, como o NSG para gerenciar o tráfego de entrada.

## Passo 6: **Configurar Balanceador de Carga**

- Para garantir alta disponibilidade, vá até **Balanceadores de Carga** no portal e clique em **Criar**.
- Escolha **Balanceador de Carga Público** ou **Balanceador de Carga Interno**, conforme necessário.
- Defina as regras de balanceamento de acordo com o tráfego e a distribuição entre máquinas virtuais.
- Associe o balanceador às suas máquinas virtuais para distribuir o tráfego de maneira eficiente.

## Passo 7: **Implementar Serviços de Banco de Dados**

- Para criar um banco de dados, pesquise por **Banco de Dados SQL** ou **Banco de Dados MySQL** no painel.
- Siga o processo de configuração, definindo nome, credenciais de administrador e parâmetros de escalabilidade.
- Associe o banco de dados à rede virtual para garantir a conectividade segura com os outros componentes da arquitetura.

## Passo 8: **Implementar Monitoramento e Logs**

- No painel do Azure, procure por **Monitor**.
- Configure **Logs de Diagnóstico** para cada recurso criado, incluindo máquinas virtuais, banco de dados e redes.
- Ative **Alertas** para monitorar métricas críticas, como uso de CPU, disco e disponibilidade de rede.
- Considere integrar com o **Azure Log Analytics** para consolidar e analisar logs em uma única interface.

## Passo 9: **Definir Backups e Redundância**

- Habilite **Backup do Azure** para suas máquinas virtuais e banco de dados.
- Configure uma política de backup automatizada que atenda às suas necessidades de recuperação.
- Considere **Replicação Geográfica** para dados críticos, garantindo recuperação em caso de falhas em uma região.

## Passo 10: **Revisar e Ajustar Configurações**

- Revise periodicamente todos os recursos, verificando se há desperdício de recursos (como VMs superdimensionadas).
- Ajuste **Autoescala** para que os recursos aumentem e diminuam de acordo com a demanda.
- Mantenha boas práticas de **segurança**, revisando os grupos de segurança e acessos periodicamente.

## Passo 11: **Manutenção Contínua e Otimização**

- Use o **Azure Cost Management** para monitorar os custos e otimizar o uso de recursos.
- Automatize processos repetitivos com **Azure Automation** ou **Runbooks**.
- Realize testes regulares de **disponibilidade e recuperação de desastres** para garantir que a arquitetura está preparada para eventos inesperados.

## Referências
- [Well-Architected Framework do Azure](https://learn.microsoft.com/pt-br/azure/architecture/framework/)
- [Conceitos básicos da arquitetura de aplicativos do Azure](https://learn.microsoft.com/pt-br/azure/architecture/guide/)
- [Procurar referências de arquiteturas do Azure - Azure Architecture Center](https://learn.microsoft.com/pt-br/azure/architecture/browse/)
- [Arquiteturas de Referência em Nuvem: conhecendo os recursos gratuitos do Azure Architecture Center](https://www.youtube.com/watch?v=nDbZMNtl8PU)
