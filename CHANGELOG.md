# Changelog

[English (US)](CHANGELOG.en-US.md) · [Distribuição oficial](https://github.com/FP-SOLU/afluente-releases/releases/latest)

Este registro descreve mudanças entregues por versão. Notas de execução e limites de validação ficam nos relatórios da release; uma correção não implica certificação de todos os provedores ou ambientes.

## 0.6.3 — 2026-11-06

### Continuidade e memória

- Substituído o recorte das últimas quatro tarefas por seleção de contexto com referências e acesso ao histórico integral do chat/projeto.
- Adicionadas busca paginada, leitura por trechos, checkpoints citados e consulta do arquivo ou imagem original.
- Preservadas orientações recentes e escolhas antigas, com origem e estado da tarefa. Registros de agentes continuam separados de autorizações humanas e memórias aprovadas.
- Credenciais de contexto acompanham o ciclo da sessão e são revogadas no encerramento/cancelamento.

### Execução e desempenho

- Detecção de repetição considera progresso observado e permite uma recuperação de estratégia antes de interromper uma repetição persistente.
- Tarefas com avanço continuam além de sete rodadas; o estado de progresso é limitado e persistente.
- Notificações da UI são agrupadas; leituras simultâneas compartilham a consulta e a janela oculta pausa a atualização visual, com recuperação ao voltar.
- Novas tarefas aguardam quando a estimativa de memória disponível não comporta outra execução, preservando o trabalho ativo.
- Sessões Codex reutilizam a thread com isolamento de agente, projeto, modelo e permissões. Uso cumulativo é convertido em consumo por execução; anexos idênticos não são reenviados à mesma thread.

### Atualização e verificação

- O atualizador busca a versão estável mais recente e reconfere o destino antes de instalar, invalidando downloads intermediários.
- Mensagens distinguem versão nova, falha de verificação e tarefas em andamento.
- Adicionadas regressões de histórico longo, imagens, isolamento, reinício, repetição, memória, sessões e rajadas de eventos. A jornada real de landing e os limites observados são registrados no relatório técnico.

## 0.6.2 — 2026-11-06

- Removidos os blocos duplicados “Resumo da tarefa” e “Entrega e evidências”; preservado “Detalhes da execução”.
- Perguntas em etapas, com retorno, respostas preservadas, envio em lote e confirmação animada.
- Ícones oficiais de provedores; organização de sessões e diagnóstico MCP; alinhamento das configurações.
- Cotas Codex/ChatGPT e Claude na lateral, quando informadas pelo provedor.

## 0.6.1 — 2026-11-06

- Opções explícitas para orientar a tarefa atual ou adicionar um novo pedido à fila, incluindo Claude.
- Refinamentos de perfis no chat e da execução de MCPs em segundo plano.

## 0.6.0 — 2026-11-06

- Evolução da experiência com múltiplos provedores, onboarding, modelos, diagnóstico de integrações e ferramentas locais.
- Conhecimento local independente do OKF e refinamentos de memória, uso e configuração.

Para versões anteriores, consulte as [releases oficiais](https://github.com/FP-SOLU/afluente-releases/releases) e os registros em `docs/`.

---
**Afluente — by FP Solutions**  
Desenvolvido e mantido pela FP Solutions.
