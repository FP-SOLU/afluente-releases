# Afluente 0.6.4

**FP Solutions · Windows x64 · 07/11/2026**

## Português (Brasil)

Esta correção trata interrupções no transporte Codex e melhora o diagnóstico quando uma tarefa não consegue terminar.

- Mensagens grandes e imagens válidas não são mais interrompidas pelo limite agregado anterior de 4 MiB. A leitura é incremental, com limite por mensagem.
- Se o processo do agente se perde antes de a aplicação começar a aguardar sua resposta, a tarefa recebe uma falha identificada.
- Detalhes da execução mostram a causa permitida informada pelo provedor, códigos técnicos e o resultado da recuperação. Dados privados de erros não são persistidos.
- Uma falha transitória terminal pode receber uma continuação na mesma thread, uma única vez. As permissões permanecem iguais. A aplicação não reenvia o pedido inteiro ou seus anexos. Decisões pendentes ou uso de comandos, MCPs, alterações de arquivo e geração no turno bloqueiam a recuperação, inclusive quando a ferramenta já concluiu.
- Cancelamento, autenticação, cotas, políticas e perda do processo mantêm suas paradas explícitas.

Atualize pelo próprio Afluente quando suas tarefas terminarem. Dados e agentes ficam separados da instalação. Uma nova versão não consegue reconstruir a causa técnica que uma versão anterior não registrou.

## English (US)

This patch addresses Codex transport interruptions and improves diagnostics when a task cannot finish.

- Valid larger messages and images no longer trip the previous aggregate 4 MiB check. Input is framed incrementally with a per-message limit.
- Losing the agent process before waiting for its response now produces an identified failure.
- Execution details retain sanitized provider failure descriptions, technical codes, and recovery results. Private error payloads are not persisted.
- A confirmed terminal transient error may receive one continuation on the same thread, with unchanged permissions. The original request and attachments are not replayed. Pending decisions or command, MCP, file-change, or image-generation activity in the turn block automatic continuation, including tools that have already completed.
- Cancellation, authentication, quotas, policies, and process loss remain explicit stopping conditions.

Update through Afluente after running tasks finish. Agents and user data remain separate from the installation. A new release cannot reconstruct diagnostics that an older release never recorded.

---
**Afluente — by FP Solutions**
