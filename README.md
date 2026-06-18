# design-web-marketing

Plugin de **landing pages, sites e marketing de conversão**, de ponta a ponta.

Um **maestro** conduz o caminho e chama a skill especialista certa em cada etapa. A voz e o
modelo de negócio saem do **seu** contexto (gerado pela skill `product-marketing`), então a copy
sai adaptada ao seu negócio — não a um SaaS genérico.

## ⚡ Instalar (copia e cola)

No Claude Code, cola uma linha por vez:

```
/plugin marketplace add cassianodiniz/cassiano.diniz
/plugin install design-web-marketing@cassiano.diniz
```

Depois **reinicie o Claude Code**. Comece rodando `design-web-marketing:product-marketing` uma vez
— ela cria o contexto do seu negócio (`.agents/product-marketing.md`) que todas as outras skills leem.

## Como usar

Acione o maestro quando não souber por onde começar ou quiser o caminho inteiro:

```
/design-web-marketing:maestro
```

…ou fale direto o que quer ("monta uma landing", "estrutura a oferta", "essa página
não converte") que o maestro roteia. Etapa única e clara (ex: "só publica") pode chamar
a skill específica direto.

**Comece pela base:** rode `design-web-marketing:product-marketing` uma vez — ela cria um
arquivo `.agents/product-marketing.md` com o contexto do seu negócio (público, dor, oferta, voz)
que todas as outras skills leem. Sem ele, as skills tratam tudo como SaaS genérico.

## O que tem dentro

| Skill | Pra que serve |
|---|---|
| `design-web-marketing:maestro` | Orquestra o caminho e roteia pra skill certa, na ordem certa |
| `design-web-marketing:product-marketing` | Monta o contexto do negócio (rodar 1x — as outras leem) |
| `design-web-marketing:offers` | Estrutura a oferta: bônus, garantia, escassez, pagamento |
| `design-web-marketing:copywriting` | Escreve copy de página do zero |
| `design-web-marketing:copy-editing` | Lapida copy que já existe (7 filtros) |
| `design-web-marketing:cro` | Diagnostica por que a página não converte |
| `design-web-marketing:marketing-psychology` | Gatilhos e modelos de persuasão |
| `design-web-marketing:customer-research` | Acha a linguagem real do público |

As etapas de **design e publicação** (construir a tela, debug, deploy) ficam **fora** do plugin —
o maestro chama skills externas opcionais (ex: uma skill de design/frontend, `vercel:deploy`) se
você as tiver instaladas.

## Créditos / licença

As 7 skills de marketing são adaptadas de
[coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills)
(Corey Haines, licença MIT). Ver `CREDITS.md` e `LICENSE-marketingskills`.
