# 🐟 Focus Group IA — o "MiroFish" caseiro, direto no Claude Code

Roda um **grupo de pesquisa virtual** com o seu público-alvo, dentro do Claude Code,
sem ferramenta paga. Você dá a oferta (produto, preço, promessa, avatar) e o Claude:

1. monta um painel de **8 a 12 personas diversas** do seu público;
2. faz **cada uma reagir sozinha** à sua oferta (agentes independentes, sem efeito manada);
3. te entrega um **relatório de objeções, ângulos que vendem, disposição a pagar e
   recomendações acionáveis** — antes de você gastar 1 real em tráfego.

É o mesmo conceito do MiroFish, mas: **grátis** (roda no seu próprio Claude Code),
**rápido** (minutos) e **auditável** (você lê a resposta de cada persona).

---

## Por que isso funciona

O segredo é cada persona reagir **isolada** — nenhuma vê a resposta da outra. É o que
gera diversidade real de opinião em vez de um eco otimista. E o relatório trata as
**rejeições como o ouro**: as objeções de quem NÃO compra são o que te faz ajustar a
oferta antes de queimar verba.

> ⚠️ Focus group (real ou de IA) **superestima intenção de compra**. O valor não é o
> número absoluto de conversão — é o **mapa de objeções e ângulos**. Use pra decidir
> headline, prova, garantia, preço e segmentação, não pra prever faturamento.

---

## Instalação (30 segundos)

Copie a pasta `focus-group-ia/` para as skills do seu Claude Code:

```bash
# opção global (vale pra todos os projetos)
cp -r focus-group-ia ~/.claude/skills/

# ou por projeto
cp -r focus-group-ia .claude/skills/
```

Pronto. O Claude Code passa a reconhecer a skill.

---

## Como usar

Basta pedir em linguagem natural — o Claude aciona a skill sozinho:

```
Roda um focus group da minha oferta: [cola aqui o produto, preço, promessa e quem é o público]
```

ou aponte pra uma página/doc:

```
Faz um focus group virtual dessa página de vendas: https://...
Meu público é [descreve o avatar].
```

O Claude vai (se faltar algo essencial, pergunta uma vez), montar o painel, rodar as
personas em paralelo e te entregar o relatório. Se quiser, peça no fim:

```
Agora roda de novo com a headline reposicionada e compara.
```

---

## O que você recebe

- **Tabela do painel** — cada persona e sua probabilidade de compra
- **Atrações** — o que vende (pra amplificar)
- **Objeções** — o que trava, por frequência
- **Disposição a pagar** — o preço é barreira? pra quem?
- **Order bumps / upsells** — qual pega, qual afasta
- **Recomendações acionáveis** — 5 a 8 mudanças concretas, cada uma amarrada à objeção
  que resolve

Veja `exemplo-relatorio.md` pra um relatório real (anonimizado).

### Preview de uma saída real

```
Painel (8 personas) e probabilidade de compra
┌──────────────────────────────┬───────┐
│ cliente ideal (dor exata)    │  82%  │
│ compradora serial de curso   │  88%  │
│ jovem, quer escalar          │  68%  │
│ nativa digital, cética preço │  55%  │
│ leiga em tech, orçam. curto  │  35%  │
│ veterana, cética com "robô"  │  35%  │
└──────────────────────────────┴───────┘

Objeção nº1 (5/8): "vou conseguir fazer sozinha?" → material gravado sem suporte assusta
Achado de posicionamento: veteranas leram a promessa como "a máquina me substitui" e recuaram
Recomendação: testar 2 headlines (a atual vs. uma que mantém o cliente NO CONTROLE)
```

O ouro está nas **objeções de quem NÃO comprou** — é o que você ajusta antes de gastar verba.

---

## Dicas de quem já rodou

- **Calibre com dados reais** quando tiver (vendas passadas, pesquisa de cliente) — aí
  as personas param de ser achismo e viram projeção ancorada.
- **Rode 2 versões** pra decisão de risco (ex.: 2 headlines, 2 preços) e compare os vereditos.
- **Inclua sempre "votos de não"** — se todas as personas comprarem, o painel tá viciado
  e não serve. A skill já força isso.

---

Feito pela **[dig.D](https://digd.com.br)** 🐱 — método de validar oferta antes de gastar
tráfego. Fica à vontade pra adaptar ao seu nicho.
