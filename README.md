# MN: skills do Claude Code

Skills e ferramentas que eu uso no Claude Code, num lugar só, para não pesar os outros repositórios.

| Skill | Para que serve | Origem e licença |
| --- | --- | --- |
| `hallmark` | Criar e redesenhar páginas web com cara de feitas à mão, não geradas (`/hallmark`). | [Nutlope/hallmark](https://github.com/Nutlope/hallmark), commit 04977e1, MIT |
| `reverse-engineer-anything` | Engenharia reversa de programas, apps e sites com o REA. Vem com o servidor MCP `rea`. | [morluto/rea](https://github.com/morluto/rea), `rea-agents` 6.10.1, MIT |

## Instalar no computador

Precisa do [Claude Code](https://code.claude.com) e do Node.js 18 ou mais novo.

Dentro do Claude Code, rode:

```
/plugin marketplace add lipedubas-tech/mn
/plugin install ferramentas@mn
```

Depois reinicie o Claude Code. As skills valem em todos os projetos.

Para atualizar quando este repositório mudar: `/plugin marketplace update mn`.

### Opcional

- **Hallmark conferindo a página no navegador:** `npm i -g puppeteer-core`, com o Chrome instalado. Sem isso, ela faz só as verificações de código.
- **REA analisando programas compilados:** precisa do Ghidra, do Hopper ou do IDA. Para sites e JavaScript não precisa de nada.

## Cuidados

- O REA serve só para analisar programas que são seus ou que você tem autorização para examinar.
- O código analisado pelo REA é enviado ao modelo de IA.
- O servidor `rea` roda pelo `npx` com a versão fixada (6.10.1). Para atualizar, troque o número em `ferramentas/.mcp.json`.
