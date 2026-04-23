# 📦 Claude Skills — Ecossistema Jarvis

**45 Repositórios + 1553 Skills + 10 Agentes AIOX + Memory Persistente**

Um ecossistema completo de desenvolvimento com IA orquestrado.

---

## ⚡ Quick Start

```bash
# Clone com todos os 45 submódulos
git clone --recurse-submodules https://github.com/Yuri-Fernando/Claude_Skills
cd Claude_Skills

# Cada submódulo está pronto para usar
# Veja instruções abaixo
```

---

## 🎯 O Que Tem Aqui

- **45 Repositórios** — frameworks, tools, skills, agents, MCPs
- **1553 Skills** — discoverable via `/find-skills` em Claude Code
- **10 Agentes AIOX** — @dev, @qa, @architect, @pm, @po, @sm, @analyst, @data-engineer, @ux-design, @devops
- **3 MCP Servers** — GitNexus, OmniRoute, obsidian-master-kit
- **Memory Persistente** — user.md, decisions.md, preferences.md sincronizados entre dispositivos
- **Graphify Integration** — 71.5x token economy reduction (20.000 → 280 tokens/session)

---

## 📂 45 Repositórios (Submódulos)

### 🏗️ Frameworks Core (6)

| Repo | Descrição | Uso |
|------|-----------|-----|
| **aios-core** | AIOX Framework — agentes, tasks, workflows | Arquitetura base para IA agents |
| **antigravity-kit** | 20+ agentes + 37 skills + 11 workflows patterns | Referência de padrões AIOX |
| **claude-code-templates** | Templates pré-pronto para projetos | Iniciar novo projeto em 2min |
| **get-shit-done** | GSD workflow — análise técnica completa | Planning, research, execution |
| **claude-mem** | Memory system para Claude | Persistência entre sessões |
| **rtk** | AI orchestration toolkit | Agentes e workflows |

### 🎬 Video Generation (3)

| Repo | Descrição | Uso |
|------|-----------|-----|
| **higgsfield-seedance2-jineng** | 15 video generation skills (Seedance 2.0) | `/cinematic`, `/3d-cgi`, `/anime-action`, etc |
| **remotion** | Programmatic video generation | Criar vídeos via código |
| **skyreels-v2** | AI video creation | Geração automática de conteúdo |

### 🧠 Code Intelligence (5)

| Repo | Descrição | Uso |
|------|-----------|-----|
| **GitNexus** | MCP Server — indexing, graph, análise | `gitnexus index .` para entender arquitetura |
| **graphify** | Knowledge graph (AST + semantic) | `/graphify . --watch` para grafo persistente |
| **context7** | Library documentation lookup | Docs de qualquer biblioteca |
| **everything-claude-code** | Claude Code tips & tricks | Referência de features |
| **planning-with-files** | File-based planning system | Organizar projetos |

### 👥 Agent Orchestration (4)

| Repo | Descrição | Uso |
|------|-----------|-----|
| **pixel-agents** | VS Code extension — visualizar agentes | Typing, reading, waiting states em tempo real |
| **awesome-agent-skills** | Coleção de skills para agentes | Referência de implementações |
| **agent-skills-for-context-engineering** | Skills context-aware | Agentes com contexto arquitetural |
| **agent-skills-context-engineering** | Agent skill patterns | Padrões reusáveis |

### 🌐 AI Infrastructure (4)

| Repo | Descrição | Uso |
|------|-----------|-----|
| **OmniRoute** | MCP Server — AI gateway com 100+ providers | Dashboard em http://localhost:3000, fallback automático |
| **firecrawl-claude-plugin** | Web scraping + crawling | Dados estruturados de qualquer URL |
| **obsidian-master-kit** | MCP Server — Obsidian setup + sync | `/obsidian-master-kit:init` em 5 minutos |
| **n8n-mcp** | Workflow automation — MCP server | Integração com n8n |

### 🎓 Skills & Templates (9)

| Repo | Descrição | Uso |
|------|-----------|-----|
| **anthropics-skills** | Official skills from Anthropic | Base de referência |
| **antigravity-awesome-skills** | 37 specialized skills | Encontrar via `/find-skills` |
| **awesome-claude-skills** | Comunidade: melhores skills | Inspiração e patterns |
| **awesome-claude-code** | Comunidade: tips Claude Code | Learn best practices |
| **obsidian-skills** | Skills para Obsidian | Automação em Obsidian |
| **notebooklm-skill** | NotebookLM integration | Análise de documentos |
| **trailofbits-skills** | Security & audit skills | Análise de segurança |
| **marketingskills** | Marketing automation | Growth strategies |
| **claude-skills** | Coleção de skills | Repository padrão |

### 🔧 Specialized Tools (5)

| Repo | Descrição | Uso |
|------|-----------|-----|
| **MiroFish** | Multi-agent prediction + swarm simulation | `upload seed → describe prediction → get simulation` |
| **OpenSpec** | Spec framework (artifact-guided development) | `/opsx:propose`, `/opsx:apply`, `/opsx:archive` |
| **refine** | React/Next framework para UI | Building production UIs |
| **context-mode** | Context-aware operations | Detectar contexto automaticamente |
| **ui-ux-pro-max-skill** | UX/UI design principles | Design system patterns |

### 📈 Marketing & Growth (5)

| Repo | Descrição | Uso |
|------|-----------|-----|
| **ai-marketing-claude** | AI marketing automation | Campaigns, content, strategy |
| **ai-sales-team-claude** | Sales team orchestration | Outreach, follow-up, closing |
| **goviralbro** | Viral content generation | Social media optimization |
| **ralph-claude-code** | Code + marketing integration | Docs + marketing sync |
| **massgen** | Bulk generation framework | Create at scale |

### 🎨 Design & UX (3)

| Repo | Descrição | Uso |
|------|-----------|-----|
| **superpowers** | Design system framework | UI components + tokens |
| **superpowers-marketplace** | Design marketplace | Browse, download, customize |
| **ui-ux-pro-max-skill** | Design skill library | UX patterns + best practices |

### 🌟 Misc (1)

| Repo | Descrição | Uso |
|------|-----------|-----|
| **xquads-squads** | Squad orchestration | Team coordination patterns |

---

## 🚀 Como Usar

### 1. **Descobrir Skills Corretas**

```bash
# Em qualquer projeto com .claude/
/find-skills "sua tarefa aqui"
→ Mostra 10+ skills com relevância score

# Se nenhuma atender:
/skill-forge "preciso de [capacidade]"
→ Cria nova skill automaticamente
```

### 2. **Usar Agentes AIOX**

```bash
@dev           # Implementação de código
@qa            # Testes e validação  
@architect     # Design técnico
@pm            # Product management
@po            # Product owner
@sm            # Scrum master
@analyst       # Pesquisa
@data-engineer # Banco de dados
@ux-design     # UX/UI design
@devops        # CI/CD, git push (exclusivo)

# Ativar com:
@dev *help     # Ver comandos do agente
@dev *task {nome}  # Executar task específica
```

### 3. **Usar MCP Servers**

```bash
# GitNexus — entender arquitetura
gitnexus index .
gitnexus serve

# OmniRoute — AI gateway
omniroute start
# Dashboard: http://localhost:3000

# Obsidian Master Kit — setup
/obsidian-master-kit:init
/obsidian-master-kit:sync
```

### 4. **Integrar em Novo Projeto**

```bash
# Copie .claude/ para seu projeto
cp -r Claude_Skills/.claude/ seu-projeto/.claude/

# Customize config.yaml
# Pronto! Tem acesso a:
# - 1553 skills
# - 10 agentes
# - Memory persistente
# - Graphify (71.5x menos tokens!)
```

### 5. **Memory Persistente**

Seus projetos têm acesso automático a:

```
G:\Claude\memory\
├── user.md (perfil + contexto)
├── decisions.md (decisões técnicas +30d review)
├── preferences.md (feedback + regras)
└── Obsidian Vault/ (sincronizado bidirecional)
```

**Sincronização automática:**
- File layer: memory/user.md, decisions.md
- Vault layer: Obsidian bi-directional sync
- Cloud layer: MongoDB + Supabase

---

## 📚 Documentação Completa

- **[INSTALLATION.md](INSTALLATION.md)** — Setup passo-a-passo
- **[MASTER-INDEX.md](MASTER-INDEX.md)** — Todas as 45 repos com descrições detalhadas
- **[MCP-SERVERS.md](MCP-SERVERS.md)** — GitNexus, OmniRoute, obsidian-master-kit
- **[SKILLS-REFERENCE.md](SKILLS-REFERENCE.md)** — Índice das 1553 skills por categoria

---

## 💡 Token Economy: Graphify

Redução de **71.5x tokens** por sessão:

```
❌ SEM SYSTEM:
   10 sessões/dia × 20.000 tokens = 200.000 tokens
   Custo/mês: ~$18

✅ COM SYSTEM:
   Sessão 1: 20.000 tokens (construir graph uma vez)
   Sessões 2-10: 280 tokens cada (consultar graph)
   10 sessões/dia = 21.100 + (9 × 1.380) = 33.520 tokens
   Custo/mês: ~$3
   
   ECONOMIA: 83% menos tokens
   APÓS 1 MÊS: ~135.000 tokens total (44.4x menos!)
```

Como funciona:
1. Memory auto-load (user.md + decisions.md) = 1.100 tokens
2. Graphify consulta graph.json = 280 tokens
3. Total sessão: 270 tokens (vs 20.000 sem sistema!)

---

## 🔄 Fluxo Típico

```
1. Novo projeto? 
   → cp -r .claude/ seu-projeto/.claude/

2. Nova tarefa?
   → /find-skills "sua tarefa"
   → Seleciona skill correta
   → @dev implementa
   → @qa testa
   → @devops push

3. Decisão importante?
   → Salva em memory/decisions.md
   → Sync automático para Obsidian + MongoDB
   → Próximo projeto herda conhecimento
```

---

## 📊 Status

| Componente | Versão | Status |
|-----------|--------|--------|
| 45 Repos | ✅ | Todos como submódulos |
| 1553 Skills | ✅ | `/find-skills` discovery |
| 10 Agentes | ✅ | @agent-name activation |
| 3 MCPs | ✅ | GitNexus, OmniRoute, obsidian-master-kit |
| Memory | ✅ | 4-layer sync (file, vault, cloud) |
| Graphify | ✅ | 71.5x token reduction |

---

## 📝 License

Composite repository — cada submódulo retém sua própria license.

---

**Versão:** 1.0  
**Data:** 2026-04-22  
**Tipo:** 45 repos + 1553 skills + 10 agentes + memory persistente

*Synkra AIOX + Graphify + Obsidian Master Kit*
