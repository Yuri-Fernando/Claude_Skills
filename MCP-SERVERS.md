# 🔌 MCP Servers Guide

Guia completo dos 3 MCP servers integrados ao Jarvis Ecosystem.

---

## 📌 O Que São MCPs?

**Model Context Protocol servers** (MCPs) são ferramentas que estendem capacidades de Claude conectando APIs externas, bancos de dados, e sistemas via protocolo padrão.

No Jarvis Ecosystem, temos 3 MCPs fundamentais:

1. **GitNexus** — Code intelligence, indexing, graph
2. **OmniRoute** — AI gateway, multi-provider fallback
3. **obsidian-master-kit** — Obsidian sync, curation

---

## 🧠 GitNexus — Code Intelligence

**Repo:** `Claude_Skills/GitNexus/`  
**GitHub:** https://github.com/abhigyanpatwari/GitNexus  
**Tipo:** MCP Server para análise de código  
**Função:** Entender arquitetura, dependências, patterns

### Instalação

```bash
cd Claude_Skills/GitNexus
npm install -g .
```

### Uso

```bash
# Indexar um projeto
gitnexus index /seu/projeto

# Serve para Claude Code
gitnexus serve
# Default: http://localhost:6001

# Verificar versão
gitnexus --version
```

### Configuration (.claude/settings.json)

```json
{
  "mcp_servers": {
    "gitnexus": {
      "command": "gitnexus",
      "args": ["serve"],
      "env": {
        "GITNEXUS_PORT": "6001"
      }
    }
  }
}
```

### O Que Faz

| Operação | Resultado |
|----------|-----------|
| `index .` | Build full dependency graph |
| `analyze` | Architecture patterns + tech debt |
| `diff` | Compare branches/tags |
| `search` | Find symbols, functions, dependencies |
| `metrics` | Cyclomatic complexity, LOC, etc |

### Exemplo Prático

```bash
# Novo projeto
cd /projeto/novo
gitnexus index .
# → Gera graph.json com toda arquitetura

# Pergunta em Claude Code
# "Qual é a arquitetura?" 
# → GitNexus fornece contexto completo
```

### Benefício

✅ Agentes têm **visibilidade 100%** da arquitetura  
✅ Sem gaps ou missed dependencies  
✅ Decisões informadas por dados reais  

---

## 🌐 OmniRoute — AI Gateway

**Repo:** `Claude_Skills/OmniRoute/`  
**GitHub:** https://github.com/diegosouzapw/OmniRoute  
**Tipo:** MCP Server para roteamento multi-provider  
**Função:** Fallback automático entre 100+ AI providers

### Instalação

```bash
cd Claude_Skills/OmniRoute
npm install -g .
```

### Iniciar

```bash
omniroute start
# Dashboard: http://localhost:3000

# Ou em modo CLI
omniroute
```

### Configuration

**Setup de providers (CLI):**

```bash
omniroute config add claude
omniroute config add gpt-4
omniroute config add gemini
omniroute config add o1
```

**Setup de fallback chain:**

```bash
omniroute fallback:add claude-opus → claude-sonnet → gpt-4-turbo
omniroute fallback:add local-llm → claude → gpt-4
```

**Em .claude/settings.json:**

```json
{
  "mcp_servers": {
    "omniroute": {
      "command": "omniroute",
      "args": ["serve"],
      "env": {
        "OMNIROUTE_DASHBOARD": "http://localhost:3000",
        "FALLBACK_CHAIN": "claude-opus,claude-sonnet,gpt-4"
      }
    }
  }
}
```

### Uso em Claude Code

```bash
# Via MCP
omniroute ask "minha pergunta"

# Com provider específico
omniroute ask --provider gpt-4 "pergunta"

# Com fallback (tenta claude, depois sonnet, depois gpt-4)
omniroute ask --fallback "pergunta"
```

### Matriz de Providers

| Provider | Suporte | Tipo |
|----------|---------|------|
| Claude (Opus/Sonnet/Haiku) | ✅ | Nativo |
| GPT-4 / GPT-3.5 | ✅ | OpenAI |
| Gemini | ✅ | Google |
| o1 | ✅ | OpenAI |
| Llama | ✅ | Meta |
| Local LLM | ✅ | Ollama/Llamafile |
| Anthropic API | ✅ | Direct |
| ... | ✅ | 100+ total |

### Fallback Automático

```
Pergunta do usuário
    ↓
Tenta Provider 1 (Claude)
    ├─ Sucesso? → Retorna resposta
    └─ Falha (rate limit, error)? ↓
Tenta Provider 2 (Sonnet)
    ├─ Sucesso? → Retorna resposta
    └─ Falha? ↓
Tenta Provider 3 (GPT-4)
    ├─ Sucesso? → Retorna resposta
    └─ Falha? → Error ao usuário
```

### Benefício

✅ **Resiliência:** Fallback automático em caso de rate limits  
✅ **Economia:** Usa provider mais barato disponível  
✅ **Flexibilidade:** Trocar provider sem código  
✅ **100+ providers:** Suporta qualquer modelo moderno  

---

## 📚 Obsidian Master Kit — Obsidian Setup

**Repo:** `Claude_Skills/obsidian-master-kit/`  
**GitHub:** https://github.com/melgarafael/obsidian-master-kit  
**Tipo:** MCP Server para Obsidian setup + curation  
**Função:** Setup, sync, AI curation de Obsidian vaults

### Instalação

```bash
cd Claude_Skills/obsidian-master-kit
npm install -g .
```

### Primeiros Passos

```bash
# Setup novo Obsidian vault
/obsidian-master-kit:init

# Ou sync existente
/obsidian-master-kit:sync
```

### Uso

```bash
# CLI
obsidian-master-kit init
obsidian-master-kit sync
obsidian-master-kit curate

# Em Claude Code
/obsidian-master-kit:init
/obsidian-master-kit:index
/obsidian-master-kit:curate
```

### Funcionalidades

| Comando | O Que Faz |
|---------|-----------|
| `:init` | Criar novo vault estruturado (1 min) |
| `:sync` | Sincronizar com Memory/Storage |
| `:index` | Index all files para buscas |
| `:curate` | AI-powered curation (relacionar notes) |
| `:backup` | Backup to cloud (MongoDB/Supabase) |
| `:link` | Auto-link relacionados |

### Vault Structure (Automática)

```
Obsidian Vault/
├── 00-Inbox/          # Capture rápida
├── 10-Pessoas/        # Contatos
├── 20-Projetos/       # Contexto de projetos
├── 30-Memoria/        # ← Sync com memory/
├── 40-Decisoes/       # ← Sync com decisions.md
├── 50-Skills/         # Índice de skills
├── 60-Agentes/        # Índice de agentes
└── 70-References/     # Papers, docs
```

### Sync Bidirecional

```
memory/user.md ←→ Obsidian/30-Memoria/user.md
memory/decisions.md ←→ Obsidian/40-Decisoes/decisions.md
memory/preferences.md ←→ Obsidian/30-Memoria/preferences.md
```

### AI Curation

```bash
# Auto-link related notes
obsidian-master-kit curate --auto-link

# Summarize folder
obsidian-master-kit curate --summarize 20-Projetos

# Find disconnected notes
obsidian-master-kit curate --find-orphans
```

### Configuration (.claude/settings.json)

```json
{
  "mcp_servers": {
    "obsidian": {
      "command": "obsidian-master-kit",
      "args": ["serve"],
      "env": {
        "OBSIDIAN_VAULT": "~/obsidian-vault",
        "AUTO_SYNC": "true",
        "SYNC_INTERVAL": "60"
      }
    }
  }
}
```

### Benefício

✅ **Setup rápido:** 1 minuto, not 30 minutos  
✅ **Sync automático:** Memory ↔ Obsidian bidirecional  
✅ **AI Curation:** Relacionar notes automaticamente  
✅ **Backup cloud:** MongoDB + Supabase  

---

## 🔄 Integração Entre MCPs

### Fluxo Completo: Novo Projeto

```
1. Clone Claude_Skills
2. Setup MCP Servers
   ├─ gitnexus index .
   ├─ omniroute start
   └─ obsidian-master-kit:init
3. Agentes têm acesso a:
   ├─ GitNexus → full code graph
   ├─ OmniRoute → 100+ AI providers
   └─ Obsidian → memory + docs
4. /find-skills descobre capacidades
5. @dev implementa com contexto total
```

### Tabela de Quando Usar

| Cenário | MCP Usar |
|---------|----------|
| "Qual é a arquitetura?" | GitNexus |
| "Claude Opus não responde" | OmniRoute fallback |
| "Organizar meus documentos" | Obsidian Master Kit |
| "Encontrar função X" | GitNexus search |
| "Backup automático" | Obsidian backup |
| "Multi-provider setup" | OmniRoute |
| "Link notas relacionadas" | Obsidian curate |

---

## ⚙️ Troubleshooting

### GitNexus

**Problema:** "index timeout"  
**Solução:** Use `--shallow` para projetos grandes
```bash
gitnexus index . --shallow
```

**Problema:** "port 6001 already in use"  
**Solução:**
```bash
lsof -i :6001  # Find process
kill -9 <PID>  # Kill it
```

### OmniRoute

**Problema:** "Provider rate limited"  
**Solução:** Fallback chain: `claude → sonnet → gpt-4`
```bash
omniroute fallback:add claude-opus → claude-sonnet → gpt-4
```

**Problema:** "Dashboard not loading"  
**Solução:**
```bash
omniroute start --port 3001  # Try different port
```

### Obsidian Master Kit

**Problema:** "Sync not updating"  
**Solução:**
```bash
obsidian-master-kit sync --force
```

**Problema:** "Notes not linked"  
**Solução:**
```bash
obsidian-master-kit curate --auto-link
```

---

## 📖 Referências

- **GitNexus:** https://github.com/abhigyanpatwari/GitNexus
- **OmniRoute:** https://github.com/diegosouzapw/OmniRoute
- **Obsidian Master Kit:** https://github.com/melgarafael/obsidian-master-kit
- **MCP Spec:** https://modelcontextprotocol.io

---

**Versão:** 1.0 | Data: 2026-04-23 | Synkra AIOX
