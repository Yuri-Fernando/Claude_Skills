# Claude Skills — Ecossistema Jarvis

### Infraestrutura modular e em evolução contínua para desenvolvimento com IA agentiva

## Status Atual

🔵 **Pesquisa / P&D — Ecossistema ativo e em evolução contínua**

O **Claude Skills — Ecossistema Jarvis** é uma infraestrutura experimental para desenvolvimento assistido por IA, reunindo **skills, agentes, MCP servers, sistemas de memória, ferramentas de contexto, workflows e componentes de automação** em uma arquitetura modular baseada em Git e submódulos.

Atualmente, o ecossistema integra **45 repositórios**, organizados como componentes reutilizáveis para desenvolvimento com IA agentiva.

Esse número **não é fixo**. Novos repositórios, ferramentas, frameworks, agentes, MCP servers e capacidades são continuamente avaliados e incorporados conforme novas necessidades, experimentos e oportunidades de integração surgem.

### Estado atual

| Componente                  | Estado atual                 |
| --------------------------- | ---------------------------- |
| **45 Repositórios**         | ✅ Integrados                 |
| **1553 Skills**             | ✅ Disponíveis para discovery |
| **10 Agentes AIOX**         | ✅ Integrados                 |
| **3 MCP Servers**           | ✅ Integrados                 |
| **Memory Persistente**      | ✅ Ativo                      |
| **Graphify**                | ✅ Integrado                  |
| **Expansão do ecossistema** | 🔄 Contínua                  |

```text
45 Repos atuais
      ↓
Avaliação de novas ferramentas
      ↓
Integração de novos componentes
      ↓
Novos agentes / skills / MCPs
      ↓
Atualização da infraestrutura
      ↓
Ecossistema em evolução contínua
```

> **45 repositórios é o estado atual do ecossistema — não o estado final.**

---

# Objetivo

A proposta do projeto é construir uma camada própria e reutilizável de infraestrutura para **IA agentiva**, reduzindo o acoplamento a uma única ferramenta, modelo, framework ou fornecedor.

O ambiente é estruturado para experimentar e integrar diferentes agentes e runtimes, incluindo:

* Claude;
* Codex;
* OpenCode;
* OpenClaw;
* Hermes;
* Agentes próprios;
* Arquiteturas experimentais no estilo **Jarvis**.

A ideia é evoluir de um conjunto de ferramentas isoladas para uma infraestrutura capaz de organizar:

```text
Agent
   ↓
Orchestration
   ↓
Skills / Tools
   ↓
Memory / Context
   ↓
MCP / APIs
   ↓
Execution
   ↓
Observability / Knowledge
```

---

# O que este ecossistema reúne

O ambiente atual integra:

* **45 repositórios** como submódulos Git;
* **1553 skills** para descoberta de capacidades;
* **10 agentes AIOX** especializados;
* **3 MCP servers**;
* memória persistente;
* Graphify para contexto estrutural;
* ferramentas de planejamento;
* ferramentas de engenharia de software;
* automação;
* componentes de marketing;
* componentes de design;
* ferramentas de pesquisa e análise.

---

# Arquitetura

```text
                         Claude Skills
                              │
             ┌────────────────┼────────────────┐
             │                │                │
             ▼                ▼                ▼
         Skills           AI Agents         MCP Servers
             │                │                │
             └────────────────┼────────────────┘
                              ▼
                       Orchestration Layer
                              │
             ┌────────────────┼────────────────┐
             ▼                ▼                ▼
          Memory          Graphify           Tools
             │                │                │
             └────────────────┼────────────────┘
                              ▼
                     Project Execution
                              │
                              ▼
                     Knowledge / Logs
```

A arquitetura foi construída para permitir a inclusão, substituição ou evolução de componentes sem reestruturar integralmente o ambiente.

---

# Quick Start

## Clone com todos os submódulos

```bash
git clone --recurse-submodules https://github.com/Yuri-Fernando/Claude_Skills
cd Claude_Skills
```

Caso o repositório já tenha sido clonado sem os submódulos:

```bash
git submodule update --init --recursive
```

Para atualizar os componentes:

```bash
git submodule update --remote --merge
```

---

# Frameworks Core

| Repositório               | Descrição                                   | Uso                             |
| ------------------------- | ------------------------------------------- | ------------------------------- |
| **aios-core**             | AIOX Framework — agentes, tasks e workflows | Arquitetura base para agentes   |
| **antigravity-kit**       | Agentes, skills e workflow patterns         | Referência arquitetural         |
| **claude-code-templates** | Templates para projetos                     | Inicialização de projetos       |
| **get-shit-done**         | Workflow de planejamento e execução         | Planning / Research / Execution |
| **claude-mem**            | Sistema de memória para Claude              | Persistência entre sessões      |
| **rtk**                   | AI orchestration toolkit                    | Agentes e workflows             |

---

# Video Generation

| Repositório                     | Descrição                     | Uso                 |
| ------------------------------- | ----------------------------- | ------------------- |
| **higgsfield-seedance2-jineng** | Skills para geração de vídeo  | Criação audiovisual |
| **remotion**                    | Geração programática de vídeo | Vídeo via código    |
| **skyreels-v2**                 | AI video creation             | Geração de conteúdo |

---

# Code Intelligence

| Repositório                | Descrição                                  | Uso                       |
| -------------------------- | ------------------------------------------ | ------------------------- |
| **GitNexus**               | MCP para indexing e graph analysis         | Entendimento arquitetural |
| **graphify**               | Knowledge graph baseado em AST + semântica | Contexto persistente      |
| **context7**               | Consulta de documentação                   | Library knowledge         |
| **everything-claude-code** | Patterns e boas práticas                   | Referência Claude Code    |
| **planning-with-files**    | Planejamento baseado em arquivos           | Organização de projetos   |

---

# Agent Orchestration

| Repositório                              | Descrição                          | Uso                    |
| ---------------------------------------- | ---------------------------------- | ---------------------- |
| **pixel-agents**                         | Visualização de agentes no VS Code | Estados de execução    |
| **awesome-agent-skills**                 | Coleção de skills                  | Referência             |
| **agent-skills-for-context-engineering** | Skills context-aware               | Engenharia de contexto |
| **agent-skills-context-engineering**     | Padrões reutilizáveis              | Agent Context Patterns |

---

# AI Infrastructure

| Repositório                 | Descrição               | Uso                    |
| --------------------------- | ----------------------- | ---------------------- |
| **OmniRoute**               | MCP Server / AI Gateway | Multi-provider routing |
| **firecrawl-claude-plugin** | Web crawling            | Coleta de dados        |
| **obsidian-master-kit**     | MCP + Obsidian          | Knowledge management   |
| **n8n-mcp**                 | MCP para automação n8n  | Workflow integration   |

---

# Skills & Templates

| Repositório                    | Descrição                    | Uso                 |
| ------------------------------ | ---------------------------- | ------------------- |
| **anthropics-skills**          | Skills oficiais da Anthropic | Referência          |
| **antigravity-awesome-skills** | Skills especializadas        | Discovery           |
| **awesome-claude-skills**      | Skills da comunidade         | Patterns            |
| **awesome-claude-code**        | Recursos Claude Code         | Best practices      |
| **obsidian-skills**            | Skills para Obsidian         | Automação           |
| **notebooklm-skill**           | Integração NotebookLM        | Análise documental  |
| **trailofbits-skills**         | Security / Audit skills      | Segurança           |
| **marketingskills**            | Marketing automation         | Growth              |
| **claude-skills**              | Coleção de skills            | Base do ecossistema |

---

# Specialized Tools

| Repositório             | Descrição                                 | Uso                      |
| ----------------------- | ----------------------------------------- | ------------------------ |
| **MiroFish**            | Multi-agent prediction + swarm simulation | Simulações               |
| **OpenSpec**            | Spec-driven development                   | Planejamento e execução  |
| **refine**              | Framework React/Next                      | Construção de interfaces |
| **context-mode**        | Operações context-aware                   | Context management       |
| **ui-ux-pro-max-skill** | Skills de UI/UX                           | Design system            |

---

# Marketing & Growth

| Repositório              | Descrição                     | Uso                  |
| ------------------------ | ----------------------------- | -------------------- |
| **ai-marketing-claude**  | Automação de marketing        | Campaigns / Content  |
| **ai-sales-team-claude** | Orquestração de vendas        | Outreach / Follow-up |
| **goviralbro**           | Geração de conteúdo viral     | Social Media         |
| **ralph-claude-code**    | Integração código + marketing | Sync                 |
| **massgen**              | Geração em escala             | Bulk generation      |

---

# Design & UX

| Repositório                 | Descrição               | Uso                |
| --------------------------- | ----------------------- | ------------------ |
| **superpowers**             | Design system framework | UI components      |
| **superpowers-marketplace** | Marketplace             | Browse / Customize |
| **ui-ux-pro-max-skill**     | Biblioteca de design    | UX patterns        |

---

# Misc

| Repositório       | Descrição           | Uso               |
| ----------------- | ------------------- | ----------------- |
| **xquads-squads** | Squad orchestration | Team coordination |

---

# Skills Discovery

Uma das principais funções do ecossistema é permitir descoberta de capacidades de acordo com a tarefa.

```text
/find-skills "sua tarefa aqui"
```

Esse fluxo permite procurar skills relevantes antes da implementação.

Caso nenhuma capacidade existente atenda ao problema:

```text
/skill-forge "preciso de [capacidade]"
```

A proposta é tratar **capability discovery** como parte do processo de engenharia.

---

# Agentes AIOX

O ambiente possui 10 agentes especializados:

```text
@dev
@qa
@architect
@pm
@po
@sm
@analyst
@data-engineer
@ux-design
@devops
```

Exemplos:

```text
@dev *help
```

```text
@dev *task {nome}
```

Cada agente possui responsabilidades específicas dentro do fluxo de desenvolvimento.

---

# MCP Servers

O ecossistema atual integra três MCP servers principais.

## GitNexus

Indexação e entendimento estrutural do projeto:

```bash
gitnexus index .
gitnexus serve
```

---

## OmniRoute

Gateway para múltiplos provedores de IA:

```bash
omniroute start
```

Dashboard:

```text
http://localhost:3000
```

---

## Obsidian Master Kit

Inicialização:

```text
/obsidian-master-kit:init
```

Sincronização:

```text
/obsidian-master-kit:sync
```

---

# Integração em Novos Projetos

A infraestrutura pode ser incorporada a um novo projeto pela camada `.claude`:

```bash
cp -r Claude_Skills/.claude/ seu-projeto/.claude/
```

Depois, o projeto pode utilizar as capacidades configuradas pelo ecossistema.

Exemplo:

```text
seu-projeto/
└── .claude/
    ├── skills/
    ├── agents/
    ├── memory/
    └── config/
```

---

# Memory Persistente

O ambiente possui uma camada de memória persistente para manter informações relevantes entre sessões e projetos.

Estrutura:

```text
G:\Claude\memory\
├── user.md
├── decisions.md
├── preferences.md
└── Obsidian Vault/
```

### Camadas de persistência

```text
File Layer
     ↓
Vault Layer
     ↓
Cloud Layer
```

Cloud:

```text
MongoDB + Supabase
```

### Conteúdo persistido

* Perfil;
* Contexto;
* Decisões técnicas;
* Preferências;
* Regras;
* Feedback;
* Conhecimento de projeto.

---

# Graphify

O **Graphify** adiciona uma camada de conhecimento estrutural ao ambiente utilizando:

* AST;
* relações entre arquivos;
* relações semânticas;
* contexto arquitetural.

### Fluxo

```text
Codebase
   ↓
AST + Semantic Analysis
   ↓
Knowledge Graph
   ↓
Relevant Context
   ↓
Agent
```

O projeto registra uma redução de **71,5× no volume de tokens consultados por sessão**, de acordo com o cenário descrito na implementação.

O objetivo é reduzir a quantidade de contexto bruto necessária para que um agente compreenda a estrutura relevante de um projeto.

---

# Fluxo Típico

```text
1. Novo projeto
        ↓
2. Adicionar .claude/
        ↓
3. /find-skills
        ↓
4. Selecionar capacidades
        ↓
5. @architect
        ↓
6. @dev
        ↓
7. @qa
        ↓
8. @devops
        ↓
9. Memory / Decisions
        ↓
10. Graphify / Knowledge
```

A proposta é fazer com que o agente participe de etapas como:

* planejamento;
* implementação;
* validação;
* documentação;
* memória;
* manutenção;
* entendimento arquitetural.

---

# Infraestrutura Independente de Fornecedor

Um dos princípios centrais desta linha de P&D é evitar dependência rígida de uma única empresa, modelo ou plataforma.

A infraestrutura é projetada para permitir experimentação com diferentes ambientes:

```text
Claude
Codex
OpenCode
OpenClaw
Hermes
Jarvis / Agents próprios
        ↓
┌────────────────────────────────┐
│   Agentic AI Infrastructure     │
├────────────────────────────────┤
│ Skills                         │
│ Agents                         │
│ MCP                            │
│ Memory                         │
│ Context                        │
│ Graph                          │
│ Tools                          │
│ Orchestration                  │
└────────────────────────────────┘
```

A ideia é construir componentes reutilizáveis que possam ser integrados a diferentes agentes, modelos e runtimes.

---

# O que este projeto demonstra

* Engenharia de infraestrutura para IA agentiva;
* Arquitetura modular;
* Orquestração de agentes;
* Engenharia de contexto;
* Sistemas de memória persistente;
* Knowledge Graphs;
* MCP;
* Tool integration;
* Workflow orchestration;
* Provider-agnostic architecture;
* Integração entre agentes e ferramentas;
* Desenvolvimento assistido por IA;
* Organização de ecossistemas Git;
* Automação de workflows de engenharia;
* Experimentação com diferentes runtimes.

---

# Estrutura Geral

```text
Claude_Skills/
│
├── .claude/
│   ├── agents/
│   ├── skills/
│   ├── memory/
│   └── config/
│
├── submodules/
│   ├── aios-core/
│   ├── claude-mem/
│   ├── GitNexus/
│   ├── graphify/
│   ├── OmniRoute/
│   ├── obsidian-master-kit/
│   └── ...
│
├── INSTALLATION.md
├── MASTER-INDEX.md
├── MCP-SERVERS.md
├── SKILLS-REFERENCE.md
└── README.md
```

---

# Documentação

* **[INSTALLATION.md](INSTALLATION.md)** — Setup e configuração;
* **[MASTER-INDEX.md](MASTER-INDEX.md)** — Índice dos repositórios;
* **[MCP-SERVERS.md](MCP-SERVERS.md)** — MCP servers integrados;
* **[SKILLS-REFERENCE.md](SKILLS-REFERENCE.md)** — Índice das skills.

---

# Status Atual do Ecossistema

| Componente                  | Estado        |
| --------------------------- | ------------- |
| **45 Repositórios**         | ✅ Integrados  |
| **1553 Skills**             | ✅ Disponíveis |
| **10 Agentes AIOX**         | ✅ Integrados  |
| **3 MCP Servers**           | ✅ Integrados  |
| **Memory Persistente**      | ✅ Ativa       |
| **Graphify**                | ✅ Integrado   |
| **Expansão do ecossistema** | 🔄 Contínua   |

### Evolução contínua

```text
45 Repos atuais
      ↓
Avaliação de novas ferramentas
      ↓
Integração de novos componentes
      ↓
Novos agentes / skills / MCPs
      ↓
Atualização da infraestrutura
      ↓
Novo estado do ecossistema
      ↓
Repetição contínua
```

> **45 repositórios representam o estado atual do ecossistema, não o estado final.**

O conjunto é tratado como um **laboratório vivo de Agentic AI**, no qual novos componentes podem ser incorporados, substituídos ou reorganizados continuamente.

---

# Roadmap de P&D

A evolução do ecossistema está concentrada em:

* Maior abstração entre agentes e providers;
* Runtimes independentes;
* Orquestração entre agentes heterogêneos;
* Evolução da memória persistente;
* Knowledge Graphs mais completos;
* Avaliação automática de agentes;
* Observabilidade de workflows agentivos;
* Agent-to-Agent communication;
* Execução local-first;
* Infraestrutura para agentes próprios;
* Novas integrações conforme o ecossistema evolui.

A direção é evoluir de um conjunto integrado de ferramentas para uma **infraestrutura modular própria para Agentic AI**.

---

# Licença

**Composite repository**

Cada submódulo mantém sua própria licença e seus próprios termos de uso.

Consulte o repositório correspondente antes de redistribuir ou incorporar qualquer componente.

---

# Autor

**Yuri Fernando Dubbern**

AI/ML Engineer · Generative AI · AI Agents · Data Engineering · Intelligent Automation

[LinkedIn](https://www.linkedin.com/in/yuridubbern) · [GitHub](https://github.com/Yuri-Fernando) · [Lattes](http://lattes.cnpq.br/7151392692642166) · [Linktree](https://linktr.ee/yuri.f.dubbern)

---

> **Este repositório faz parte de uma linha contínua de P&D em infraestrutura para IA agentiva.**
>
> O objetivo é construir uma camada própria de **skills, agentes, memória, contexto, ferramentas e orquestração**, capaz de evoluir continuamente e permanecer independente de um único fornecedor de IA.
