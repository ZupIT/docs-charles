---
title: Release Notes
weight: 98
description: Nesta seção, você encontra o Release Notes do CharlesCD.
---


{{% release/group %}}

{{% release/item type="feature" date="Maio 2021" %}}

Criação do CI/CD para staging.

Atualização do helm values.yaml.

Aumento do tempo de timeout padrão.

Atualização do CI de charts e changelog.

Atualização da release do pipeline.
{{% /release/item %}}
 
{{% release/item repository="Butler" date="Maio 2021" %}}
Adição Butler operator.

Adição de logs de evento do Butler.

Charlescd release 1.0.0.

Adição de notificação do módulo de eliminação.

Adição da notificação de undeploy do Moove.

Classificação dos registros por data.

Adicionar Mock Service Worker na IU.
{{% /release/item %}} 

{{% release/item repository="UI" date="Maio 2021" %}}
Adição do suporte para o protocolo HTTP.

Adição validação de comprimento máximo para campos de entrada.

Atualização do routing quando a clicar na conta. 

Mostrar a notificação quando apagar.

Adição do novo serviço para encontrar dados dos círculos simplificados. 

Mostrar a notificação quando o webhook é deletado. 

Adição da validação isNotBlank para o nome dos Workspaces criados.

Adição de responsividade para mudar a senha.

Adição da margem para legenda no modo de edição.

Adição minLength para a descrição do workspace.
{{% /release/item %}}

{{% release/item repository="GATE" date="Maio 2021" %}}
Adição workspace id para autorizar requisições e negar requisições de log.

Adição System Token.

Adição de notificação no módulo de excluir. 

Adição do campo de configuração de deployment.
{{% /release/item %}}

{{% release/item repository="MOOVE" date="Maio 2021" %}}
Charlescd: release 0.7.1.

Adição do patch de deployment ativo para remover a configuração de deployment. 

Adição da validação quando a configuração de deployments estiver ativa. 
{{% /release/item %}}

{{% release/item repository="MOOVE" date="Abril 2021" %}}
Adição de logs de deploy.

Sincronizar as informações do circle matcher quando criar ou excluir. 
{{% /release/item %}}

{{% release/item repository="UI" date="Abril 2021" %}}
Adição do módulo Webhook.

Sincronizar as informações do circle matcher quando criar ou excluir. 

Adição de qual versão do Charles você está.
{{% /release/item %}}

{{% release/item repository="Butler" date="Abril 2021" %}}
Adição da estrátegia de porcentagem de deployment. 
{{% /release/item %}}


{{% release/item type="fix" repository="UI" date="Maio 2021" %}}
Bump ssri da 6.0.1 para 6.0.2 in /ui.

Correção do modelo de grupo de usuários.

Correção das opções de módulo e componentes.

Correção de erros e itens de layout.

Correção do deployment de namespaced.

Correção da atualização do menu do workspace.

Correção das ações na lista dos círculos.

Correção da permissão do grupo de usuário e criação de um modal para remoção desse grupo. 

Correção de erro de build error e como salvar uma ação.

Correção UI webhook.

Correção do alinhamento vertical para o InputTitle.

Correção da ações de métricas.

Correção defaultValue para o perfil da conta.

{{% /release/item  %}}

{{% release/item repository="Moove" date="Maio 2021" %}}
Auth e token agora são anuláveis.

Correção do teste do system token que estava quebrado para os logs de deployments e atualização dos serviços. 

Melhoria nas mensagens de erro do moove.

Correção da atualização do matcher csv.

Manipulação do erro de template.

Correção na configuração de validação do deployment na atualização do workspace. 

Correção exclusão do usuário do grupo de usuários.

Correção validação de exclusão de configuração.

Correção da consulta da query.

Correção valor do tempo de execução.

Correção das mensagens de erro.

Correção da edição do nome do grupo de usuários.

Correção da versão semver para o validador csv.

Correção CSV validador de versão.

Correção da atualização do matcher.

Correção do status do workspace.
{{% /release/item  %}}

{{% release/item date="Maio 2021" %}}
Correção da permissão de configurações do Gate em values.yaml.

Correção da instalação v1.0 do Helm.

Correção das permissões para query do workspace. 

Correção do papel do cluster para o Butler, adicionando acesso para todos os grupos de API.

Correção da pipeline.

Correção na atualização da autorização.

Correção do chart.
{{% /release/item  %}}

{{% release/item repository="Butler" date="Maio 2021" %}}
Bump y18n da 4.0.0 para 4.0.3 in /butler.

Correção do erro de git.

Mudança do token, gatewayName e a validação do valor do host.

Correção do serviço de log.

Manipular erro de template. 

Correção da requisição do moove do git token base64.

Correção erro quando a URL do Helm é inválida. 

Correção substituição de namespace "deadlock".

Correção do erro de cache.

Correção do erro de lint e o envio do UNDEPLOY_FAILED por padrão.

Correção de mensagens de erro.

Correção edição do nome do grupo de usuários.
{{% /release/item  %}}

{{% release/item repository="Moove" date="Maio 2021" %}}
Remoção da opção 'criado' da estrutura de permissão.

Correção da regeneração do token sistêmico.

Correção token sistêmico.

Correção método errado nas políticas csv.
{{% /release/item  %}}

{{% release/item repository="UI" date="Abril 2021" %}}
Correção [Grupo de usuário] para evitar a lista duplicada após atualizações.

Correção botão ativado / desativado ao criar um novo usuário.

Correção da criação de círculo a partir do arquivo CSV.

[Grupo de usuário] Permissão para o mantenedor remover grupos de from Workspace.

Correção mostrando nome de usuário indefinido na tela inicial.

Correção exibição do menu de forma inconsistente para o caminho root.

Correção para mostrar 'obrigatório' no campo opcional quando registrar um módulo.

{{% /release/item  %}}

{{% release/item repository="Butler" date="Abril 2021" %}}
Mudança de passos na pipeline do Butler.

{{% /release/item  %}}

{{% release/item repository="Moove" date="Abril 2021" %}}
Correção para obter a porcentagem do círculo no repositório. 

{{% /release/item  %}}

{{% release/item repository="Compass" date="Abril 2021" %}}
 Correção do erro no prometheus na lista de métricas.

{{% /release/item  %}}

{{% release/item repository="Hermes" date="Abril 2021" %}}
 Correção do erro no prometheus na lista de métricas.

{{% /release/item  %}}

{{% release/item type="chore" repository="UI" date="Maio 2021" %}}
UI Operator.

Remoção do código legado e scroll infinito. 

Mudança dos pacotes de gerenciamento de UI de yarn para npm.

Mudança de texto em um botão.

Teste de exceção useUpdateName.

Melhoria no texto do botão de criação de token. 

Atualização do menu do usuário depois de modificar qualquer usuário. 

Desativar botão de deploy.

Atualização do menu do usuário alterando o nome.

Mudança do texto isNotBlank de 'No whitespace' para 'Cannot start with whitespaces'.

Definir o campo da branch como obrigatório.

Melhoria do Wizard.
{{% /release/item  %}}

{{% release/item repository="Moove" date="Maio 2021" %}}
Remoção de id desnecessário do log da resposta. 

Exclusão da configuração de deployment. 

Melhoria das entidades duplicadas. 

Atualização da versão do Keycloak.

Alteração dos registros definidos para garantir ordem.

Exclusão do usuário root padrão.

Substituição das dependências do validador csv.
{{% /release/item  %}}

{{% release/item repository="Gate" date="Maio 2021" %}}
Atualização da política de adição de postagem no workspace para a função de gerenciamento. 

{{% /release/item  %}}

{{% release/item repository="Butler" date="Maio 2021" %}}
Validação das tags em letras maiúsculas.

Configuração do limite de tamanho da requisição do Butler para 50mb por padrão.

Bump lodash da 4.17.19 para 4.17.21 no Butler.
{{% /release/item  %}}

{{% release/item repository="Villager" date="Maio 2021" %}}
Remoção de dependencias não utilizadas do Villager.

{{% /release/item  %}}

{{% release/item date="Maio 2021" %}}
Atualização do envvar skip SSL.

Melhoria do trigger de CI para o bug-hunting.
{{% /release/item  %}}

{{% release/item repository="UI" date="Abril 2021" %}}

Remoção do recurso de hipóteses.

Melhorias as opções avançadas na tela do componente. 

Remover ações da guia do módulo ao criá-lo.

Atualizar os scripts-react de 4.0.1 a 4.0.3.

Bump node-notificador de 8.0.0 para 8.0.1 no /ui.

Bump elíptico de 6.5.3 to 6.5.4 no /ui.
{{% /release/item  %}}

{{% release/item repository="Butler" date="Abril 2021" %}}
Execução de filtros do Butler.
{{% /release/item  %}}

{{% release/item type="docs" date="Outubro 2021" %}}
  Migração da documentação do Gitbook para o Hugo. 
  {{% /release/item  %}} 

{{% /release/group %}}

Acess a página de [**Release Notes do CharlesCD**](https://github.com/ZupIT/charlescd/releases).
