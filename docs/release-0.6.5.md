# Afluente 0.6.5

**FP Solutions · Windows x64 · 07/11/2026**

## Português (Brasil)

Corrige a experiência de atualização quando uma prévia antiga permanece com encerramento incerto.

- Antes de fechar, o Afluente confere a identidade dos serviços e suas portas. Se houver pendência, mantém a janela aberta e indica a porta e o painel Ambiente da conversa para revisão.
- A verificação não mata processos desconhecidos, não arquiva registros por conta própria e não declara encerramento a partir apenas de um PID ausente.
- O botão mostra a preparação e impede pedidos simultâneos. As tarefas continuam protegidas contra instalação durante execução.
- Ao sair, o app aguarda todos os recursos e gravações. Uma falha isolada não antecipa a saída enquanto outras operações ainda terminam.
- Um relatório local identifica a etapa que ficou sem confirmação; dados privados de erros não entram nesse relatório.

Atualize pelo próprio Afluente. Caso sua versão anterior já tenha fechado com uma pendência, reabra e confira Ambiente da conversa antes de tentar novamente. Registros sem processo correspondente podem ser arquivados após revisão explícita, sem encerrar processos.

## English (US)

Fixes the update experience when an older preview record remains in an uncertain shutdown state.

- Before closing, Afluente checks service identities and ports. Pending records keep the window open with the port and conversation environment panel identified for review.
- The check does not kill unknown processes, automatically archive records, or treat a missing PID alone as confirmed cleanup.
- Preparation feedback prevents concurrent requests. Running tasks continue to block installation.
- Shutdown waits for every resource and persistence operation. An isolated failure cannot finish shutdown while other operations are still settling.
- A local report identifies the unconfirmed stage without retaining private error payloads.

Update through Afluente. If an older version already closed because of a pending record, reopen it and review the conversation environment before retrying. Records without a matching process can be archived after explicit review without terminating processes.

---
**Afluente — by FP Solutions**
