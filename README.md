# Afluente

**Um espaço para pessoas e agentes trabalharem juntos.**  
Desenvolvido pela **FP Solutions** · Windows x64 · Versão 0.6.4

[English (US)](README.en-US.md) · [Baixar a última versão](https://github.com/FP-SOLU/afluente-releases/releases/latest) · [Changelog](CHANGELOG.md)

## Trabalhe com uma equipe, em uma conversa

Reúna agentes com funções, instruções, skills e modelos próprios. Converse em canais ou mensagens diretas, envie referências e acompanhe entregas, decisões e arquivos no mesmo lugar. Codex, Claude Code e APIs compatíveis podem coexistir na equipe; cada agente usa a conexão configurada para ele.

### O que está disponível

- **Conversa e continuidade:** menções, encaminhamento entre especialistas, histórico consultável, orientações durante a execução e fila persistente. Decisões, imagens e arquivos mantêm referências à sua origem.
- **Controle de execução:** perguntar, revisão automática ou acesso total no compositor; perguntas críticas em etapas; aprovações vinculadas à solicitação; cancelamento e retomada.
- **Missões e rotinas:** etapas, checkpoints, horários e quadro com arraste. Conclusão manual fica identificada; efeitos incertos após uma queda exigem revisão.
- **Navegador e prévias locais:** navegador por conversa/projeto, acompanhamento visual, entrada manual e persistência opcional de sessão. Serviços supervisionados continuam entre passagens de agentes.
- **Arquivos e conhecimento:** anexos, prints colados, imagens ampliáveis, visualização de texto/Markdown, versões por hash, fontes locais e memória revisável. O OKF é opcional.
- **Equipe configurável:** modelos por provedor, skills, MCPs selecionados, instruções editáveis, avatares e ferramentas de navegador/computador local.
- **Uso e distribuição:** cotas quando informadas pelo provedor, atualizações no aplicativo e instalador próprio Afluente.

## Começar

1. Baixe o instalador no [canal oficial](https://github.com/FP-SOLU/afluente-releases/releases/latest).
2. Informe seu nome e o espaço de trabalho; a foto é opcional.
3. Conecte um ou mais provedores, crie seu primeiro agente e abra a primeira conversa.
4. Vincule a pasta do projeto, envie o objetivo e defina as permissões no compositor.

As CLIs mantêm a autenticação com seus fornecedores. Chaves de API são protegidas pelo Windows e não acompanham a exportação da equipe. Perfis e arquivos de trabalho ficam separados da instalação.

Para um trabalho completo, explique o resultado esperado, as restrições e como verificar a entrega. Você pode corrigir a direção durante a tarefa sem reenviar todo o briefing. Consulte o [guia de condução](docs/conduzir-trabalho-no-afluente.md).

## Novidades da 0.6.4

Transporte Codex corrigido para mensagens grandes e perda de processo; falhas com causa permitida e persistente; uma continuação controlada para erros transitórios, respeitando permissões, cancelamento e efeitos sem confirmação. Mantidos o histórico consultável, checkpoints, proteção por progresso e atualização direta da 0.6.3. Veja as [notas da versão](docs/release-0.6.4.md).

## Operação e limites

O Afluente executa localmente: precisa estar aberto, inclusive na bandeja, para trabalhar. Desligar o computador encerra a execução. Navegador e compute são configuráveis; não há computador remoto incluído.

Uma conexão configurada ou um catálogo de modelos não comprovam uma inferência bem-sucedida. Visão, geração de imagens, MCPs e cotas dependem do modelo, da conexão e das permissões. O aplicativo informa capacidades ausentes. Não copia automaticamente credenciais OAuth de ferramentas externas.

Histórico e checkpoints não concedem novas permissões. Memória reutilizável exige revisão. Arquivos removidos ou fora do escopo não podem ser recuperados pela simples existência de uma referência. Rotinas e provedores corporativos precisam ser conferidos no computador de destino.

## Desenvolvimento

```powershell
npm ci
npm run typecheck
node --test --test-concurrency=1 tests/*.test.cjs
npm run build
npm run desktop
```

`npm run dev` abre somente a prévia da interface. Testes Electron usam perfis descartáveis e distinguem transportes simulados de chamadas a provedores reais. Para empacotar no Windows, consulte o [runbook de release](docs/atualizacoes-e-release.md). O build do instalador requer Python/fontTools e as ferramentas WPF/.NET Framework; o aplicativo instalado não exige Node ou Python separados.

## Atualizações e dados

O aplicativo consulta o canal público, avisa e oferece download e instalação explícitos. A partir da 0.6.3, reconfere a última versão antes de instalar e recusa um download intermediário desatualizado. A instalação aguarda o fim das tarefas. Assinatura digital do instalador e validação em segundo computador permanecem etapas separadas.

Código-fonte privado em `FP-SOLU/afluente`; distribuição pública em `FP-SOLU/afluente-releases`. Não publique perfis, credenciais ou capturas privadas. Faça backup antes de downgrade: versões antigas podem não aceitar dados mais novos.

[Inventário funcional](INVENTARIO.md) · [Pesquisa de contexto](research/2026-11-06-continuidade-contexto-memoria.md)

---
**Afluente — by FP Solutions**  
Desenvolvido e mantido pela FP Solutions.
