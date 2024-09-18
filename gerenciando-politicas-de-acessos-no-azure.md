# Desafio de projeto
Tutorial do Desafio de projeto **Gerenciando Políticas de Acessos no Azure** desenvolvido durante o Bootcamp Microsoft Azure Essentials na DIO

## Passo 1. Entenda o Controle de Acesso Baseado em Funções (RBAC)

O **RBAC (Role-Based Access Control)** é o modelo de gerenciamento de permissões no Azure. Ele permite atribuir funções específicas a usuários, grupos ou aplicativos, restringindo ou concedendo permissões.

- No **RBAC**, as permissões são definidas por **funções**.
  - Exemplos de funções:
    - **Owner**: Acesso total para gerenciar recursos.
    - **Contributor**: Pode criar e gerenciar recursos, mas não alterar permissões.
    - **Reader**: Pode visualizar recursos, mas não modificar.

## Passo 2. Atribua Funções a Usuários e Grupos

Você pode atribuir funções diretamente a usuários, grupos ou identidades gerenciadas.

- No portal do Azure, navegue até o **Recurso** ou **Grupo de Recursos** que deseja gerenciar.
- Clique em **Controle de Acesso (IAM)**.
- Selecione **Adicionar Atribuição de Função**.
  - Escolha uma função, como **Leitor** ou **Contribuidor**.
  - Selecione o usuário ou grupo ao qual deseja conceder a função.
- Confirme a atribuição clicando em **Salvar**.

## Passo 3. Utilize Políticas do Azure (Azure Policy)

As **políticas do Azure** ajudam a impor regras e garantir a conformidade em toda a sua organização. Com as políticas, você pode restringir determinadas ações ou exigir que certas condições sejam atendidas.

- No portal do Azure, procure por **Políticas**.
- Clique em **Atribuições de Política**.
- Selecione **Atribuir Política** e escolha o **escopo** da política, como uma assinatura ou grupo de recursos.
  - Exemplo de política: **Exigir tag em recursos** ou **Restringir o tipo de máquina virtual**.
- Defina os parâmetros da política, se aplicável, e clique em **Revisar e Criar**.

## Passo 4. Monitore o Acesso com Azure Active Directory (Azure AD)

O **Azure Active Directory** (Azure AD) é o serviço de gerenciamento de identidade e acesso do Azure. Ele permite gerenciar quem tem acesso a quais recursos e monitorar atividades.

### Adicione Usuários:
- No portal do Azure, vá até **Azure Active Directory** > **Usuários**.
- Selecione **Novo Usuário** para adicionar um novo usuário à sua organização.
- Preencha as informações necessárias, como nome, email e função inicial.

### Gerencie Grupos:
- Em **Azure AD**, vá até **Grupos**.
- Crie um novo grupo para organizar usuários com permissões semelhantes.
- Atribua funções de acesso a esses grupos para simplificar o gerenciamento.

## Passo 5. Configure Políticas de Condição de Acesso

As **políticas de condição de acesso** permitem aplicar regras específicas baseadas em condições, como local, dispositivo ou aplicativo utilizado.

- No portal do Azure, vá para **Azure Active Directory** > **Segurança** > **Condições de Acesso**.
- Crie uma nova política clicando em **Nova Política**.
- Defina **Usuários e Grupos** aos quais a política será aplicada.
- Configure as condições, como o local do usuário (Ex: restringir o acesso fora do escritório) ou o aplicativo utilizado.
- Configure os controles de acesso: exija autenticação multifator (MFA) ou bloquear acesso.
- Salve e ative a política.

## Passo 6. Revise Logs de Auditoria e Acessos

O **Azure Monitor** e os **Logs de Auditoria** permitem que você monitore a atividade de acesso e faça auditoria de alterações em políticas de segurança.

- No portal do Azure, vá para **Monitor** > **Logs de Auditoria**.
- Visualize as atividades relacionadas a acessos e permissões, como:
  - Quem atribuiu uma função a determinado usuário.
  - Quais políticas foram aplicadas ou alteradas.

## Passo 7. Aplique a Prática de Privilégio Mínimo

Para garantir a segurança, siga a prática de **privilégio mínimo** ao atribuir acessos.

- Atribua apenas as permissões necessárias para que os usuários executem suas funções.
- Evite conceder permissões de **Owner** ou **Contributor** se o acesso de leitura for suficiente.

## Passo 8. Revise Periodicamente as Políticas de Acesso

Realize revisões periódicas das atribuições de acesso e políticas para garantir que os usuários continuem tendo apenas as permissões necessárias.

- No portal do Azure, em **Controle de Acesso (IAM)**, revise todas as atribuições de função.
- Use o **Azure AD Access Reviews** para identificar e remover acessos desnecessários automaticamente.

## Dicas
- Ao atribuir funções em níveis mais altos, como em uma **Assinatura**, os usuários herdarão essas permissões em todos os recursos dentro dessa assinatura.
- Configurar alertas para ser notificado sobre eventos específicos, como a atribuição de uma função crítica.
- Criar uma política que force a aplicação de tags a todos os recursos, facilita a organização e monitoramento de custos.
- **MFA** (autenticação multifator) é uma medida de segurança eficaz para proteger contas com mais de um fator de autenticação.
- Usar o **Azure Policy** ajuda a avaliar a conformidade e impor padrões organizacionais. O painel de conformidade fornece uma visão geral do ambiente e permite avaliar a granularidade por política ou recurso. 
- Criar as **definições de iniciativa**, é possível agrupar várias definições de política para alcançar uma meta geral. 
- Usar o **Microsoft Entra ID** para centralizar controles de segurança e detecções de identidades de serviço e de usuário

## Referências
- [Saiba mais sobre o Microsoft Purview](https://learn.microsoft.com/en-us/purview/purview)
- Conceitos básicos do Microsoft Azure: Descrever o gerenciamento e a governança do Azure
   - [Unidade 1 - Introdução](https://learn.microsoft.com/training/modules/describe-cost-management-azure/1-introduction)
   - [Unidade 3 - Descrever a finalidade do Azure Policy](https://learn.microsoft.com/training/modules/describe-features-tools-azure-for-governance-compliance/3-describe-purpose-of-azure-policy)
   - [Unidade 4 - Descrever a finalidade dos bloqueios de recursos](https://learn.microsoft.com/training/modules/describe-features-tools-azure-for-governance-compliance/4-describe-purpose-of-resource-locks)
