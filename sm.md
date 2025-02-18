# Planeje e prepare-se para o ciclo de lançamentos 1 de 2024 do Microsoft Copilot Studio

- Artigo
- 31/07/2024
- 3 colaboradores

Comentários

Neste artigo[Visão geral](https://learn.microsoft.com/pt-br/power-platform/release-plan/2024wave1/microsoft-copilot-studio/#overview)[Regiões de investimento](https://learn.microsoft.com/pt-br/power-platform/release-plan/2024wave1/microsoft-copilot-studio/#investment-areas)[Para administradores de aplicativos](https://learn.microsoft.com/pt-br/power-platform/release-plan/2024wave1/microsoft-copilot-studio/#for-application-administrators)[Aproveite ao máximo o Microsoft Copilot Studio](https://learn.microsoft.com/pt-br/power-platform/release-plan/2024wave1/microsoft-copilot-studio/#get-the-most-out-of-microsoft-copilot-studio)

 Importante

O plano do ciclo de lançamentos 1 de 2024 inclui todas as novas funcionalidades planejadas para serem lançadas no mercado de abril de 2024 a setembro de 2024. Neste artigo, você encontrará a visão geral do produto, as novidades e os planos para o **Microsoft Copilot Studio**.



## Visão geral

<iframe src="https://aka.ms/ReleaseHighlight/2024W1/PowerPlatform" frameborder="0" allowfullscreen="true" data-linktype="external" style="box-sizing: inherit; outline-color: inherit; margin: 0px; padding: 0px; border: 0px; width: 640px; height: 360px; inset: 0px;"></iframe>

O Microsoft Copilot Studio (antes Power Virtual Agents) é usado para estender o Microsoft Copilot no Microsoft 365 e criar copilotos personalizados para cenários internos e externos. O Copilot Studio permite aos criadores projetar, testar e publicar copilotos usando a tela de criação abrangente. Os criadores podem criar facilmente conversas habilitadas para IA generativa, fornecer maior controle às respostas de copilotos existentes e acelerar a produtividade com fluxos de trabalho automatizados específicos.

Criar extensões para o Microsoft Copilot para Microsoft 365 é um recurso nativo do Copilot Studio; em poucos minutos, um criador pode criar um tópico com a IA generativa, descrever como ele será usado e quais recursos ele oferece, e publicá-lo no Microsoft Copilot - tudo no âmbito de controles de governança do Microsoft 365.

Os recursos de IA do Microsoft Copilot Studio podem concluir tarefas automaticamente para seus usuários – um criador de copiloto pode simplesmente expor as APIs de locatário, fluxos do Power Automate específicos da empresa ou outras ações ao copiloto. O copiloto entende a solicitação do usuário, examina sua biblioteca de ações e identifica aquelas que podem atender à solicitação. Ele faz a montagem e os reúne – e até solicita ao usuário informações adicionais necessárias para concluir a solicitação.

O Microsoft Copilot Studio também integrará e interoperará com GPTs personalizados da OpenAI, transformando o poder desses modelos em ferramentas fantásticas para criar ou ampliar copilotos. Estamos facilitando para as empresas importar e configurar modelos de GPT de lojas do OpenAI em copilotos. O copiloto será capaz de selecionar e chamar os modelos certos na sequência apropriada com base na consulta do usuário final e de orquestrar esses e outros blocos de construção do copiloto. Além disso, estamos trazendo modelos do AI Builder e novos recursos de prompt e plug-in para o Microsoft Copilot Studio. Com isso, os autores do copiloto e do plugin podem extrair dados de fontes externas usando vários conectores do Power Platform, permitindo respostas de IA mais precisas e específicas ao contexto. A criação de prompts permitirá a autores projetar, criar e testar prompts de IA generativa. Os criadores podem salvar prompts para facilitar a reutilização, o arquivamento e aprimoramentos futuros em prompts. Os prompts salvos darão suporte a práticas e atualizações seguras de implantação do Gerenciamento do ciclo de vida do aplicativo (ALM). Os prompts podem ser invocados em copilotos por meio de plug-ins.

O ciclo de lançamentos 1 de 2024 contém:

- Recursos nativos para estender o Microsoft Copilot
- Suporte IVR em conjunto com o Dynamics Customer Service
- Disponibilidade geral para ações generativas, geoexpansões para Emirados Árabes Unidos, Alemanha
- Recursos de gerenciamento do ciclo de vida do software, incluindo importação e exportação em nível de tópico e controle de acesso baseado em função (RBAC)
- Melhorias na governança e administração, incluindo controles de gerenciamento de IA mais granulares; logs de auditoria no Microsoft Purview, controles específicos sobre a visualização da transcrição

[![Assinatura RSS](https://learn.microsoft.com/pt-br/power-platform/release-plan/media/feed-icon.png)](https://go.microsoft.com/fwlink/?linkid=2261125) Atualizações do ciclo de lançamentos 1 de 2024 do Microsoft Copilot Studio



## Regiões de investimento

![Regiões de investimento](https://learn.microsoft.com/pt-br/power-platform/release-plan/media/whatsnewandplanned.jpg)

**Inovação do Copilot e da IA**
O Microsoft Copilot Studio sempre esteve na vanguarda de como a IA pode ser aproveitada para produzir respostas convincentes e apropriadas às perguntas e aos problemas dos usuários de bot. O Copilot Studio integra o que há de mais moderno em tecnologias de IA generativa usando modelos GPT para criar copilotos mais conversacionais.

O [recurso de respostas generativas no Microsoft Copilot Studio](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/nlu-boost-conversations) permite especificar fontes internas e externas existentes que um copiloto pode usar para responder às perguntas de um usuário do copiloto. O recurso usa IA para criar de modo inteligente respostas totalmente conversacionais para as consultas dos usuários do copiloto, sem que os criadores de copiloto precisem primeiro criar manualmente tópicos individuais para cada eventualidade.

[Ações generativas](https://learn.microsoft.com/pt-br/microsoft-copilot-studio/advanced-generative-actions) criam conversas dinamicamente ao permitir que a IA encontre e conecte os plug-ins apropriados em tempo real. Os criadores configuram o copiloto com os plug-ins apropriados e, em seguida, usando IA generativa, o sistema determina automaticamente quais plug-ins são relevantes, quais informações eles precisam do usuário e, em seguida, orquestra a conversa e a execução dos plug-ins até que a solicitação desejada do usuário seja concluída.

**Configuração do Copilot**
A configuração de um copiloto inclui todas as configurações e capacidades que um criador usa para determinar a qual público-alvo o copiloto se dirigiria (como os canais para publicar ou os copilotos para estender), como alocar recursos entre criadores e ambientes, e como configurar comportamentos do sistema para análise, registro e retenção de dados.

**Criação básica**
Criar um copiloto usando o Microsoft Copilot Studio é fácil com a tela de criação low-code, e há várias formas de gerenciar como os tópicos interagem, como você deseja que a conversa flua e como ela deve ser.

É fácil testar o copiloto sem precisar implantá-lo totalmente sempre que você fizer uma pequena alteração. Existem também lições que orientam você por meio da criação de tópicos, de cenários simples a complexos, bem como tópicos de sistema padrão. Você também pode escolher o idioma que deseja que seu copiloto use. Variáveis e entidades tornam seu copiloto mais capaz de entender os usuários, e um conteúdo rico torna seu copiloto mais relacionável e fácil de usar.

**Serviço, runtime e governança**
O Microsoft Copilot Studio é um sistema seguro, de alta escala e altamente disponível que os clientes podem usar para fornecer copilotos para seus funcionários, outras empresas e seus clientes. Com o Copilot Studio, os clientes podem criar e estender copilotos, todos executados no serviço do Copilot Studio.

O Copilot Studio está disponível em regiões geográficas de todo o mundo, bem como nas Nuvens da Comunidade Governamental. O Copilot Studio está integrado ao Power Platform e centro de administração do Power Platform, que é um local centralizado para as necessidades de governança de uma organização, para garantir que as empresas possam confiar nos criadores quanto à construção e implantação seguras, garantindo que os dados de negócios sejam protegidos.

Para saber mais sobre o conjunto completo de recursos que está sendo entregue nesse ciclo de lançamentos, **confira o plano de lançamentos do Microsoft Copilot Studio** abaixo:

[Confira o plano de lançamentos](https://aka.ms/Plan/2024RW1/MicrosoftCopilotStudio)



## Para administradores de aplicativos

**Recursos que afetam a experiência do usuário habilitados automaticamente**
Os recursos que afetam o usuário devem ser analisados pelos administradores de aplicativos. Isso facilita o gerenciamento de alterações de versões e permite a integração bem-sucedida de novos recursos lançados no mercado. Para obter a lista completa, procure todos os recursos marcados como "Usuários, automaticamente" no plano de lançamentos.

**Recursos que devem ser habilitados por administradores de aplicativos**
Este ciclo de lançamentos contém recursos que devem ser habilitados ou configurados pelos administradores, criadores ou analistas de negócios para estarem disponíveis aos usuários. Para obter a lista completa, procure todos os recursos marcados como "Usuários por administradores, criadores ou analistas" no plano de lançamentos.

![Aproveite ao máximo o Microsoft Copilot Studio](https://learn.microsoft.com/pt-br/power-platform/release-plan/media/getmostoutofproduct.jpg)



## Aproveite ao máximo o Microsoft Copilot Studio

Expandir a tabela

| Links úteis                                                  | Descrição                                                    |
| :----------------------------------------------------------- | :----------------------------------------------------------- |
| [Plano de lançamentos](https://aka.ms/Plan/2024RW1/MicrosoftCopilotStudio) | Exiba todos os recursos incluídos no lançamento.             |
| [Licenciamento](https://aka.ms/licensing/MicrosoftCopilotStudio) | Entenda melhor como licenciar o Microsoft Copilot Studio.    |
| [Documentação do produto](https://aka.ms/documentation/MicrosoftCopilotStudio) | Localizar documentação do Microsoft Copilot Studio.          |
| [Comunidade de usuários](https://aka.ms/community/MicrosoftCopilotStudio) | Interaja com especialistas do Microsoft Copilot Studio e colegas na comunidade. |
| [Eventos futuros](https://aka.ms/events/MicrosoftCopilotStudio) | Encontre eventos presenciais e online e inscreva-se.         |
| [Avaliações de produtos](https://aka.ms/trials/MicrosoftCopilotStudio) | Introdução ao Microsoft Copilot Studio.                      |

------

## Comentários