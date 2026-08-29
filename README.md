# 🗂️ Arsenal

Catálogo pessoal de ferramentas open source de agentes de IA.

**Isto é um índice, não um acervo.** Nada de código aqui — só a referência de
onde achar, o que resolve e quando vale a pena usar. O código só desce pro disco
na hora de implementar:

```bash
git clone --depth 1 <url>
```

O `--depth 1` traz só a versão atual, sem o histórico de commits. Corta 80–90%
do tamanho na maioria dos repositórios.

---

## Agentes de codificação

### OpenHands
- **Link:** https://github.com/OpenHands/OpenHands
- **Resolve:** agente autônomo que lê uma tarefa, escreve código, roda testes e abre pull request sozinho.
- **Quando usar:** tarefa de código bem delimitada que eu não quero acompanhar passo a passo.
- **Licença:** MIT
- **Atenção:** roda em Docker, imagem pesada (vários GB). Feito pra um usuário só na própria máquina — não é multiusuário.

### Aider
- **Link:** https://github.com/Aider-AI/aider
- **Resolve:** par de programação por IA direto no terminal, com commit automático a cada alteração.
- **Quando usar:** edição de código em projeto que já existe, sem sair do terminal.
- **Licença:** Apache 2.0
- **Atenção:** sobrepõe bastante com o Claude Code. Só faz sentido se eu quiser trocar de modelo por baixo.

---

## Orquestração de agentes

### LangGraph
- **Link:** https://github.com/langchain-ai/langgraph
- **Resolve:** monta fluxos de agentes como um grafo — com estado, ciclos e ponto de retomada quando algo falha.
- **Quando usar:** fluxo com várias etapas que dependem umas das outras e precisa aguentar erro no meio.
- **Licença:** MIT
- **Atenção:** curva de aprendizado real. Overkill pra automação simples.

### CrewAI
- **Link:** https://github.com/crewAIInc/crewAI
- **Resolve:** vários agentes com papéis diferentes (pesquisador, redator, revisor) trabalhando na mesma tarefa.
- **Quando usar:** quando dividir o trabalho em papéis distintos melhora o resultado.
- **Licença:** MIT
- **Atenção:** o "usado por 60% da Fortune 500" é marketing da própria empresa, não dado auditado.

### claude-task-master
- **Link:** https://github.com/eyaltoledano/claude-task-master
- **Resolve:** quebra um prompt grande em tarefas menores e coordena a execução sobre o Claude Code.
- **Quando usar:** funcionalidade grande demais pra caber numa sessão só.
- **Licença:** verificar no repo

### Hermes Agent
- **Link:** https://github.com/NousResearch/hermes-agent
- **Resolve:** agente pessoal com memória persistente que cria e refina as próprias habilidades ao longo do uso.
- **Quando usar:** assistente de longo prazo, não tarefa pontual.
- **Licença:** MIT

---

## Automação e integrações

### n8n
- **Link:** https://github.com/n8n-io/n8n
- **Resolve:** automação visual de fluxos com centenas de integrações prontas (Telegram, planilhas, HTTP, cron).
- **Quando usar:** ligar serviços entre si sem escrever o encanamento na mão.
- **Licença:** ⚠️ **Sustainable Use License — não é open source de verdade.** Uso interno é liberado; revender como produto, não.
- **Atenção:** precisa rodar 24/7 → servidor, não a máquina pessoal. Instalado passa de 1 GB.

### Browser Use
- **Link:** https://github.com/browser-use/browser-use
- **Resolve:** agente que opera o navegador — clica, preenche formulário, extrai dados de site sem API.
- **Quando usar:** o dado que eu preciso só existe na tela, não numa API.
- **Licença:** MIT
- **Atenção:** raspagem tem limite legal e de termos de uso. Site muda de layout e o fluxo quebra.

### Cloudflare Agentic Inbox
- **Link:** https://github.com/cloudflare/agentic-inbox
- **Resolve:** cliente de e-mail auto-hospedado com agente que lê a caixa de entrada e rascunha respostas.
- **Quando usar:** referência de arquitetura de agente com estado persistente.
- **Atenção:** amarrado ao ecossistema Cloudflare (Workers, Durable Objects, R2). Não é portável.

---

## Referência

### awesome-mcp-servers
- **Link:** https://github.com/punkpeye/awesome-mcp-servers
- **Resolve:** catálogo de servidores MCP — as "tomadas" que conectam um agente a serviços externos (GitHub, Postgres, Notion, Slack).
- **Quando usar:** antes de escrever qualquer integração do zero. Provavelmente já existe.
- **Atenção:** é só uma lista. Zero código pra rodar.

---

## Regras deste catálogo

1. **Estrela no GitHub é a pasta.** Custo zero de disco, sempre atualizado.
2. **Estrela não é qualidade.** Mede quantos acharam legal, não quantos usam em produção.
3. **Antes de adotar, conferir três coisas:** data do último commit, proporção de issues abertas/fechadas, e a licença.
4. **Clonar só na hora de usar**, um por vez, com `--depth 1`.
