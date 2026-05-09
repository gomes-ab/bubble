# TGFPAR — Visualizador de Parceiros

App web para visualizar a tabela **TGFPAR** do Bubble em tempo real, com busca, filtros e estatísticas.

## Funcionalidades

- Busca por nome, CNPJ, e-mail ou código
- Filtros por status ativo/inativo e integração
- Estatísticas: total, ativos, inativos, integrados, com erro
- Tabela ordenável com paginação
- Botão de atualização manual

## Deploy no GitHub Pages

### 1. Crie o repositório

Crie um repositório público no GitHub (ex: `tgfpar-app`).

### 2. Envie os arquivos

```bash
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/tgfpar-app.git
git push -u origin main
```

### 3. Ative o GitHub Pages via Actions

No repositório, vá em **Settings → Pages** e em **Source** selecione **GitHub Actions**.

O deploy roda automaticamente a cada push na branch `main`. Após alguns segundos, o app estará disponível em:

```
https://SEU_USUARIO.github.io/tgfpar-app/
```

## Configuração da API

As credenciais do Bubble estão em `index.html`:

```js
const API   = 'https://teste-n8n-50169.bubbleapps.io/api/1.1/obj/tgfpar';
const TOKEN = 'sua_chave_aqui';
```

> ⚠️ **Atenção:** como este é um repositório público, o token ficará visível no código-fonte. Considere usar a Data API do Bubble com acesso público (sem token) ou restringir o acesso ao repositório.
