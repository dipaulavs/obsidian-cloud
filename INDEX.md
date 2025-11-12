# Obsidian Cloud - Central Vault VPS

## 📊 Status
- **Estado:** 🚀 Em deploy
- **URL:** https://obsidian.loop9.com.br
- **Repositório:** https://github.com/dipaulavs/obsidian-cloud
- **VPS Path:** `/root/obsidian-cloud`
- **Stack Name:** `obsidian`

## 🎯 Objetivo

Obsidian rodando 24/7 na VPS com sincronização automática via Obsidian Sync (assinatura paga).

**Vault centralizado em:** `/config/vault/`

**Integração com ClaudeCode:** Arquivos acessíveis via path direto na VPS

## 🏗️ Arquitetura

```
Obsidian Sync (Cloud)
        ↕
VPS (obsidian.loop9.com.br)
├── Docker: linuxserver/obsidian
├── Interface web (acesso inicial)
└── /config/vault/ ← arquivos sincronizados
        ↕
ClaudeCode acessa diretamente
```

## 🛠️ Tech Stack

- **Container:** linuxserver/obsidian (latest)
- **Proxy:** Traefik (SSL automático Let's Encrypt)
- **Porta interna:** 3000
- **Vault:** `/config/vault/`
- **Sync:** Obsidian Sync oficial

## 🚀 Deploy

**Deploy inicial:**
```bash
deploy-obsidian
```

**Acesso primeira vez:**
1. Abrir https://obsidian.loop9.com.br
2. Fazer login Obsidian Sync (sua conta)
3. Configurar vault em `/config/vault/`
4. Pronto! Nunca mais precisa acessar

## 📝 Logs de Deploy

### 2025-11-12 18:11 - Deploy Inicial
- Projeto criado em `APPS E SITES/obsidian-cloud/`
- Docker compose configurado (linuxserver/obsidian)
- CNAME: obsidian.loop9.com.br → vps.loop9.com.br
- Deploy na VPS com SSL automático
