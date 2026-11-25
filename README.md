# MN: skills do Claude Code

Skills e ferramentas que eu uso no Claude Code, num lugar só, para não pesar os outros repositórios.

| Skill | Para que serve | Origem e licença |
| --- | --- | --- |
| `hallmark` | Criar e redesenhar páginas web com cara de feitas à mão, não geradas (`/hallmark`). | [Nutlope/hallmark](https://github.com/Nutlope/hallmark), commit 04977e1, MIT |
| `reverse-engineer-anything` | Engenharia reversa de programas, apps e sites com o REA. Vem com o servidor MCP `rea`. | [morluto/rea](https://github.com/morluto/rea), `rea-agents` 6.10.1, MIT |
| `last30days` (plugin à parte) | Pesquisa o que as pessoas dizem sobre um assunto nos últimos 30 dias, no Reddit, X, YouTube, Hacker News, Polymarket, GitHub e na web (`/last30days <assunto>`). | [mvanhorn/last30days-skill](https://github.com/mvanhorn/last30days-skill), 4.6.0 (commit 7c2e1c2), MIT; sem as imagens de demonstração |

## Instalar no computador

Precisa do [Claude Code](https://code.claude.com) e do Node.js 18 ou mais novo.

Dentro do Claude Code, rode:

```
/plugin marketplace add lipedubas-tech/mn
/plugin install ferramentas@mn
```

Para a last30days, que é um plugin à parte:

```
/plugin install last30days@mn
```

Depois reinicie o Claude Code. As skills valem em todos os projetos.

Para atualizar quando este repositório mudar: `/plugin marketplace update mn`.

### Opcional

- **Hallmark conferindo a página no navegador:** `npm i -g puppeteer-core`, com o Chrome instalado. Sem isso, ela faz só as verificações de código.
- **REA analisando programas compilados:** precisa do Ghidra, do Hopper ou do IDA. Para sites e JavaScript não precisa de nada.
- **last30days:** precisa do Python 3.12 ou mais novo. Sem chaves, pesquisa no Reddit, Hacker News, Polymarket e GitHub; para o X, o YouTube, o TikTok e outros, ela pede chaves opcionais em `~/.config/last30days/.env`. Ela também instala um aviso (hook) que guarda as pesquisas prontas ao fim de cada resposta.

## Cuidados

- O REA serve só para analisar programas que são seus ou que você tem autorização para examinar.
- O código analisado pelo REA é enviado ao modelo de IA.
- O servidor `rea` roda pelo `npx` com a versão fixada (6.10.1). Para atualizar, troque o número em `ferramentas/.mcp.json`.
