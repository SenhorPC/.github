# Changelog

Todas as alterações notáveis para este projeto serão documentadas neste arquivo.

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
