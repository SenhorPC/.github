# Changelog

Todas as alterações notáveis para este projeto serão documentadas neste arquivo.

## [1.2.7] - 2024-12-14
### Melhorias
- **Dashboard**: 
  - Adicionado status "2. Pending".
    -  Utilize este status para colocar em fila tickets em que precisa executar alguma atividade ainda para avançar
- **Workflow: Followup** 
  - 20241210: Excluir o thread_id associado ao user, quando for igual ao thread_id do tickets com status "5.3. Followup Done" a mais de 2 dias.
    - Objetivo quando o cliente chamar via whatsapp, não associar á um ticket antigo, e sim começar uma nova conversa
  - 20241210: Setar o campo AI_Reply_Off para false a cada execução do followup, exceto para statis "2. Pending"
  - 20241212: Alterado followup status "5. Waiting user reply", de "5.4. folloup done" para atualizar para "5.2. Followup 2D".
    - Objetivo lembrar o cliente esta sendo encerrado.
- **Worflow: Email**
  - 20241210: Adicionado node para limpar o body do email, pois as conversas anteriores estavam atrapalhar o classificação do pedido.
  - 20241211: Retornarmos o fluxo de atendimento da versão 1.0
  - 20241211: Adicionada chamada a fluxo alternativo para testes de prompt support
  - 20241212: Nos nodes de encaminhamento para outro workflow, alterado as configurações para enviar um pedido de cada vez.
    - Objetivo simplificar o código, eliminando a necessidade de adicionar loops.
- **Workflow Email from SenhorPC**
  - 20241213: Emails respondidos pela AI, terão status alterado para "4. Verify"
    - Objetivo facilitar ao administrador revisar os envios. 
- **Workflow: Groups**
  - 20241213: Removido das respostas tudo que não fosse o resultado do prompt, exemplo: propaganda, cabeçalho, ....
- **Workflow: Error**
  - 20241213: Adicionado worklow para avisar quando ocorre um erro no fluxo Email para testar.
- **Assistant AI**
  - 20241210: Revisado formato da resposta, retirado os itens "b) Instruções" e "e) Conclusão".
    - Objetivo menos texto, mais direto ao assunto
- **Gmail**
  - Adicionado regra para list:finance@senhorp.com com anexo, adicionar marcador com "1- New", e assim, entrar no fluxo.

## [1.1.0] - 2024-12-08
### Melhorias
- **Workflow Support-email**: 
  - Reativado fluxo dedicado para o assistente especializado em solicitações do tipo Request/Pedido
  - Função whatsapp_check: Adicionado função para verificação e resposta se o user tem o numero do whatsapp gravado.
  - Função whatsapp_call: (será implementada na próxima release, para trabalhar em conjunto com item C do workflow Support-email)
  - Função thread_closed:
    - Node Ticket: update. Alterado status para 5.3. Followup Done
    - Node Ticket: update. Alterado para atualizar timestamp
- **Assistant AI**:
  - Support-Email: reescrito para fornecer agendamento, tentativa rápida e conclusão. Mais função whatsapp_check
  - Support-Whatsapp: reescrito para orientar user/cliente passo a passo

## [1.0.1] - 2024-12-07
### Corrigido
- **Bug**: Corrigido um problema no `email.json` que impedia a execução do workflow em determinadas condições.
  - **Descrição**: O bug ocorria quando mais de um email chegavam no mesmo minuto
- **Bug**: Corrigido um problema no `email.json` que acabava por processar e responder emails enviados de users tipo "Supply"
  - **Descrição**: O bug ocorria quando um email chegava de um user tipo Supply, ou mesmo quando esta desligado o AI_Reply

## [1.0.0] - 2024-12-01
### Adicionado
- Lançamento inicial do projeto com funcionalidades básicas de automação.
