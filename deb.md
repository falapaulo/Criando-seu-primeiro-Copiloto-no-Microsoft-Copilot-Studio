# Compreender códigos de erro

- Artigo
- 08/01/2025
- 5 colaboradores

Comentários

Quando um agente encontra um problema durante uma conversa, ele responde com uma mensagem que inclui um código de erro para o problema específico encontrado. Os usuários do agente devem fornecer esse código de erro ao seu administrador.

Como criador de agentes, se ocorrer um problema quando você estiver usando o painel de teste para [testar o agente](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/authoring-test-bot), você poderá ver uma mensagem com mais contexto sobre o problema, além do código de erro. Como alternativa, você pode usar o painel **Verificador de tópico** para [validar seu agente](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/authoring-topic-management#topic-errors).



## Lista de erros

- [Aplicativo Web](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/error-codes?tabs=webApp#tabpanel_1_webApp)
- [Clássica](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/error-codes?tabs=webApp#tabpanel_1_classic)
- [Teams](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/error-codes?tabs=webApp#tabpanel_1_teams)

 Observação

O termo *caixa de diálogo* usado em algumas mensagens de erro refere-se a um *tópico*.

Expandir a tabela

| Código de erro                                               | Descrição                                                    |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [ContentError](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/error-codes?tabs=webApp#contenterror) | Há um erro no conteúdo do tópico.                            |
| [DataLossPreventionViolation](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/error-codes?tabs=webApp#datalosspreventionviolation) | Ocorreu uma violação da política de prevenção contra perda de dados. |
| [FlowActionException](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/error-codes?tabs=webApp#flowactionexception) | Ocorreu um erro ao executar um [fluxo da nuvem](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/advanced-flow). |
| [FlowActionBadRequest](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/error-codes?tabs=webApp#flowactionbadrequest) | Uma solicitação feita para um [fluxo da nuvem](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/advanced-flow) foi malformada. |
| [FlowActionTimedOut](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/error-codes?tabs=webApp#flowactiontimedout) | Um [fluxo da nuvem](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/advanced-flow) levou mais de 100 segundos para ser executado e atingiu o tempo limite. |
| [InvalidContent](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/error-codes?tabs=webApp#invalidcontent) | Conteúdo inválido foi adicionado ao editor de código.        |
| [InfiniteLoopInBotContent](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/error-codes?tabs=webApp#infiniteloopinbotcontent) | Um nó foi executado muitas vezes.                            |
| [LatestPublishedVersionNotFound](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/error-codes?tabs=webApp#latestpublishedversionnotfound) | Não foi possível recuperar a versão publicada do agente.     |
| [RedirectToDisabledDialog](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/error-codes?tabs=webApp#redirecttodisableddialog) | Um tópico está [redirecionando](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/authoring-topic-management#redirect-to-another-topic) para um tópico desativado. |
| [RedirectToNonExistentDialog](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/error-codes?tabs=webApp#redirecttononexistentdialog) | Um tópico está [redirecionando](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/authoring-topic-management#redirect-to-another-topic) para outro tópico que não existe mais. |
| [SystemError](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/error-codes?tabs=webApp#systemerror) | Ocorreu um erro de sistema no Copilot Studio.                |



#### ContentError

**Mensagem de erro:** esse erro produz mensagens dinâmicas com base no contexto do erro.

**Resolução:** este é um erro genérico para problemas relacionados ao conteúdo do agente. Consulte a mensagem de erro para obter mais detalhes.

Os problemas comuns incluem:

- Um nó tem propriedades necessárias ausentes.
- Um YAML inválido foi adicionado com o [editor de código](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/authoring-create-edit-topics#edit-topics-with-the-code-editor).
- Uma [fórmula do Power Fx](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/advanced-power-fx) contém um erro.



#### DataLossPreventionViolation

**Mensagem de erro:** "Este ambiente exige que os usuários entrem antes de usar o agente. Vá para Gerenciar > Segurança > Autenticação e selecione a opção para solicitar que os usuários façam login."

**Resolução:**

- As políticas de prevenção contra perda de dados (DLP) do seu ambiente exigem que os usuários façam login. Consulte [Adicionar autenticação de usuário com o tópico do sistema de Entrada](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/advanced-end-user-authentication#add-user-authentication-with-the-sign-in-system-topic).
- Um ou mais conectores usados no agente não estão no mesmo grupo de dados. Consulte [Copilot Studioconectores](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/admin-data-loss-prevention#copilot-studio-connectors).
- Um ou mais conectores usados no agente estão bloqueados pelo administrador do locatário.



#### FlowActionException

**Mensagens de erro:**

- "Nenhuma saída foi recebida do fluxo {FlowName} ({FlowId}), embora a saída fosse esperada de acordo com a definição do agente."
- "O parâmetro de saída com o nome {ItemKey} no fluxo {FlowName} ({FlowId}) está ausente nos dados de resposta. Atualize o fluxo ou certifique-se de que o fluxo retorne esse valor."
- "O parâmetro de saída com o nome {ItemKey} no fluxo {FlowName} ({FlowId}) está ausente no esquema de saída. Atualize o fluxo."

**Resolução:**[verifique se há erros no fluxo](https://learn.microsoft.com/pt-br/power-automate/error-checker).



#### FlowActionBadRequest

**Mensagens de erro:**

- "O parâmetro com nome {KeyName} no fluxo {FlowName} ({FlowId}) foi declarado ser do tipo {ItemTypeKind}. Não há suporte a esse tipo ao invocar o Power Automate. No momento, há suporte somente a Texto, Booliano e Números."
- "O parâmetro com o nome {ItemKey} no fluxo {FlowName} ({FlowId}) está ausente na ação 'Fluxo de Chamadas'".
- "O parâmetro com nome {KeyName} no fluxo {FlowName} ({FlowId}) avaliado para o tipo {ResolveType}. Tipo esperado {ExpectedType}."
- "Houve falha na execução do fluxo {FlowName} ({FlowId}) com o código de resposta {ResponseCode}. Código de erro: {FlowErrorCode}."

**Resolução:** verifique se o [tipo básico](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/authoring-variables-about#variable-types) de todas as variáveis que você passa para o fluxo correspondem ao tipo do parâmetro.



#### FlowActionTimedOut

**Mensagem de erro:** "O fluxo com id {FlowId} expirou. Código de Erro: {FlowErrorCode}"

**Resolução:**[verifique se há erros no fluxo](https://learn.microsoft.com/pt-br/power-automate/error-checker) para entender por que o fluxo da nuvem levou mais de 100 segundos para ser executado antes de retornar ao agente. Tente otimizar a consulta e os dados retornados do sistema de back-end. Se parte da lógica do fluxo de nuvem puder continuar a ser executada após o envio de um resultado ao agente, execute essas ações após a etapa 'Retornar valores para o Copilot Studio' em seu fluxo da nuvem.



#### InvalidContent

**Mensagem de erro:** "Há um total de {TotalComponents} componentes no agente, mas nenhum é válido."

**Resolução:**[abra o editor de código](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/authoring-create-edit-topics#edit-topics-with-the-code-editor) para analisar os problemas com o conteúdo.



#### InfiniteLoopInBotContent

**Mensagem de erro:** "A ação {DialogId}.{TriggerId}.{ActionId} foi executada mais de {MaxTurnCount} vezes seguidas. Isso indica um ciclo na execução do diálogo e, portanto, a execução do diálogo será encerrada."

**Resolução:** certifique-se de que o tópico termine corretamente e leve para outros tópicos que terminam corretamente, como o tópico do sistema **Escalar**.



#### LatestPublishedVersionNotFound

**Mensagem de erro:** "Não foi possível recuperar a versão mais recente publicada do agente."

**Resolução:**[publique o agente](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/publication-fundamentals-publish-channels).



#### RedirectToDisabledDialog

**Mensagem de erro:** "O Diálogo com a ID {DialogId} está desabilitado na definição. Habilite o Diálogo antes de usá-lo."

**Resolução:**[reabilite o tópico](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/authoring-topic-management) ou [remova o nó de redirecionamento](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/authoring-create-edit-topics#delete-a-node).



#### RedirectToNonExistentDialog

**Mensagem de erro:** "O Diálogo com a ID {DialogId} não foi encontrado na definição. Verifique se o Diálogo está presente e se a ID está correta."

**Resolução:**[crie um novo tópico](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/authoring-create-edit-topics#create-a-topic) ao qual redirecionar ou [remova o nó de redirecionamento](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/authoring-create-edit-topics#delete-a-node).



#### SystemError

**Mensagem de erro:** esse erro não produz uma mensagem de erro.

**Resolução:**[Entre em contato com o suporte ao cliente](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/fundamentals-support).

------

## Comentários