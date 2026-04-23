# 📖 Installation Guide — Claude Skills Ecosystem

Passo-a-passo para clonar, instalar e começar a usar o ecossistema.

---

## ⚡ Quick Clone (2 minutos)

```bash
# Clone com todos os 45 submódulos
git clone --recurse-submodules https://github.com/Yuri-Fernando/Claude_Skills
cd Claude_Skills

# Pronto! Todos os repos estão disponíveis
ls -la  # Ver as 45 pastas de submódulos
```

---

## 🔧 Instalação Completa (10 minutos)

### 1. **Clone**
```bash
git clone --recurse-submodules https://github.com/Yuri-Fernando/Claude_Skills
cd Claude_Skills
```

### 2. **Instalar Skills Globalmente** (Opcional)
```bash
# Copiar todas as 1553+ skills para Claude
cp -r higgsfield-seedance2-jineng/skills/* ~/.claude/skills/

# Ou individual:
cp higgsfield-seedance2-jineng/skills/01-cinematic/SKILL.md ~/.claude/skills/cinematic.md
```

### 3. **Setup MCP Servers**

#### GitNexus
```bash
cd GitNexus
npm install -g .
gitnexus serve
# Adicione em ~/.claude/settings.json:
# {
#   "mcp_servers": {
#     "gitnexus": "gitnexus serve"
#   }
# }
```

#### OmniRoute
```bash
cd OmniRoute
npm install -g .
omniroute start
# Dashboard: http://localhost:3000
```

#### Obsidian Master Kit
```bash
cd obsidian-master-kit
/obsidian-master-kit:init
/obsidian-master-kit:sync
```

### 4. **Configure Memory Persistente** (Opcional)
```bash
# Link para G:\Claude\memory\ (se no mesmo sistema)
ln -s /g/Outros\ computadores/..../Claude/memory/ ./memory

# Ou manualmente: copie arquivos
# - memory/user.md
# - memory/decisions.md
# - memory/preferences.md
```

### 5. **Setup Graphify**
```bash
# Instalar (se não tiver):
pip install graphifyy

# Buildgraph
/graphify . --obsidian --update

# Watch mode (manter atualizado):
/graphify . --watch  # em outro terminal
```

---

## 📂 Estrutura Após Instalação

```
Claude_Skills/
├── README.md (este projeto)
├── INSTALLATION.md (este arquivo)
├── MASTER-INDEX.md (lista de todos os 45 repos)
├── MCP-SERVERS.md (guia dos MCP servers)
├── SKILLS-REFERENCE.md (índice de 1553+ skills)
│
├── Submódulos (45 repos):
│   ├── aios-core/ (AIOX framework)
│   ├── higgsfield-seedance2-jineng/ (15 video skills)
│   ├── GitNexus/ (MCP + code intelligence)
│   ├── pixel-agents/ (VS Code extension)
│   ├── OmniRoute/ (AI gateway)
│   ├── ... (40 mais)
│   └── xquads-squads/
│
├── graphify-out/ (gerado por /graphify)
│   ├── graph.json (grafo persistente)
│   ├── graph.html (visualização interativa)
│   └── GRAPH_REPORT.md (análise)
│
└── memory/ (se setup persistente)
    ├── user.md
    ├── decisions.md
    └── preferences.md
```

---

## 🚀 Primeiros Passos

### 1. **Explorar Skills**
```bash
# Em Claude Code com .claude/ configurado:
/find-skills "sua tarefa"
# Mostra 10+ skills com relevância
```

### 2. **Usar um Agente**
```bash
# Exemplo: code review
@qa *task "review-pr"
```

### 3. **Usar um MCP Server**
```bash
# Indexar codebase
gitnexus index /seu/projeto

# Usar AI gateway
omniroute ask "explique a arquitetura"
```

### 4. **Usar Graphify**
```bash
# Gerar grafo do seu projeto
cd /seu/projeto
/graphify . --obsidian
```

---

## 🔗 Próximos Passos

1. **Ler MASTER-INDEX.md** — Conheça todos os 45 repos
2. **Ler MCP-SERVERS.md** — Entenda como usar os MCPs
3. **Ler SKILLS-REFERENCE.md** — Descubra as 1553 skills
4. **Setup um novo projeto** — Use `.claude/` template

---

## ⚙️ Troubleshooting

### Submódulos vazios
```bash
# Se algum submódulo não foi clonado:
git submodule update --init --recursive

# Com shallow clone (mais rápido):
git clone --recurse-submodules --depth 1 https://github.com/Yuri-Fernando/Claude_Skills
```

### Espaço em disco
```bash
# 45 repos = ~10GB
# Se espaço limitado, use shallow:
git clone --recurse-submodules --depth 1 https://github.com/Yuri-Fernando/Claude_Skills
```

### Skills não funcionam
```bash
# Verificar path:
echo $HOME/.claude/skills

# Copiar manualmente:
cp higgsfield-seedance2-jineng/skills/*.md ~/.claude/skills/
```

### MCP não funciona
```bash
# Verificar se está rodando:
curl http://localhost:3000  # OmniRoute
gitnexus --version          # GitNexus

# Verificar settings.json:
cat ~/.claude/settings.json | grep -A 5 mcp_servers
```

---

## 📚 Referências

- **GitHub:** https://github.com/Yuri-Fernando/Claude_Skills
- **Docs:** README.md, MASTER-INDEX.md, MCP-SERVERS.md, SKILLS-REFERENCE.md
- **Issues/PRs:** https://github.com/Yuri-Fernando/Claude_Skills/issues

---

**Versão:** 1.0 | Data: 2026-04-23 | Synkra AIOX + Graphify
