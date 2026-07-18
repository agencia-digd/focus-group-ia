---
name: focus-group-ia
description: >-
  Roda um "focus group virtual" (estilo MiroFish) direto no Claude Code: dada uma
  OFERTA/produto e seu público-alvo, gera um painel de personas-agentes diversas,
  faz cada uma reagir à oferta de forma INDEPENDENTE (em subagentes paralelos), e
  sintetiza um relatório de objeções, ângulos vencedores, disposição a pagar e
  recomendações acionáveis. Use quando o usuário quiser validar uma oferta, headline,
  preço, página de vendas, order bumps ou campanha ANTES de gastar tráfego — ou pedir
  "focus group", "pesquisa com o público", "testar a oferta", "simular reação",
  "o que meu avatar acha disso", "mirofish".
---

# Focus Group IA — o "MiroFish" caseiro no Claude Code

Simula um grupo de pesquisa com o público-alvo usando **agentes independentes**, cada
um encarnando uma persona real do avatar. Serve pra prever reação a uma oferta/campanha
sem entrevistar gente de verdade e sem ferramenta paga.

> **Princípio central:** cada persona reage SOZINHA, sem ver as respostas das outras.
> É isso que evita o efeito manada e gera diversidade real de opinião. Não gere as
> personas "conversando entre si" — gere cada reação isolada e só depois agregue.

## Quando usar
- Validar uma oferta / preço / promessa / headline antes de lançar
- Testar uma página de vendas, VSL, criativo ou order bumps
- Descobrir as objeções reais e os ângulos que convertem
- Comparar 2 versões de posicionamento (roda 2 vezes e compara)

## O método — 4 passos

### Passo 1 — Entender a oferta (colete o mínimo, não trave)
Você precisa de: **(a)** o que é o produto/oferta, **(b)** preço, **(c)** promessa
principal, **(d)** quem é o público-alvo (avatar). Se o usuário deu uma página/doc,
leia. Se faltar algo essencial, pergunte UMA vez de forma enxuta. Se der pra inferir
com premissa razoável, infira e **declare a premissa** — não faça 5 perguntas.

### Passo 2 — Montar o painel de personas (8 a 12)
Gere personas **diversas de propósito**, variando ao longo destes eixos (escolha os
que fazem sentido pro nicho):
- **Temperatura de compra:** cliente ideal (dor exata) · morno · cético · "só olhando"
- **Relação com tecnologia:** nativo digital · usa o básico · tem medo/leigo
- **Situação financeira:** o preço não pesa · pesa · conta cada centavo
- **Comportamento de compra:** comprador impulsivo/serial · desconfiado · exigente
- **Estágio no negócio/vida:** começando · estabelecido · veterano
- **Um "voto de dissonância":** sempre inclua 2-3 personas que provavelmente NÃO
  compram — senão o resultado vira eco otimista e inútil.

Dê nome, idade e 2-3 frases de contexto de vida a cada uma. Realismo > quantidade.

### Passo 3 — Rodar as reações (subagentes em paralelo)
Dispare **um subagente por persona, todos no mesmo bloco** (paralelo). Cada subagente
recebe: (1) a persona que ele encarna, (2) a oferta, (3) as perguntas. Instrua cada um a:
- responder **100% em primeira pessoa** como aquela pessoa, NÃO como IA;
- ser **honesto e realista** — se não compraria, dizer não; nem todo mundo compra;
- usar o **vocabulário/registro** da persona.

**Perguntas padrão pra cada persona** (adapte ao caso):
1. Primeira impressão real (2-3 frases)
2. Compraria por [PREÇO]? [COMPRO / TALVEZ / NÃO] — e por quê
3. O que mais te atraiu
4. O que te fez travar / sua maior objeção
5. [se houver ângulo sensível, ex. "usar IA", "assinatura", "curso gravado"] — anima ou assusta? por quê
6. [se houver order bumps/upsells] — pegaria algum? qual?
7. Que frase/promessa faria VOCÊ clicar em comprar
8. VEREDITO: probabilidade de compra de 0 a 100%

> **Fallback sem subagentes:** se o ambiente não tiver Task/subagentes, rode as personas
> uma a uma na mesma conversa, mas processe UMA POR VEZ e não deixe uma ler a resposta
> da outra (recomece o enquadramento a cada persona).

### Passo 4 — Sintetizar (o entregável)
Agregue TODAS as respostas num relatório com:
- **Tabela do painel** (persona · perfil · probabilidade de compra)
- **Atrações recorrentes** — o que vende (manter/amplificar)
- **Objeções recorrentes** — o que trava, ordenadas por frequência
- **Disposição a pagar** — o preço é barreira? pra quem?
- **Order bumps/upsells** — qual pega, qual é rejeitado e por quê
- **Segmentações reveladas** — padrões por idade/perfil/tech
- **Recomendações acionáveis** — 5 a 8 mudanças concretas (headline, prova, garantia,
  checkout, segmentação de criativo), cada uma amarrada à objeção que resolve

## Regras de qualidade (o que separa isto de "genérico")
- **Diversidade real:** sem 12 personas parecidas. Se todas comprarem, o painel tá viciado.
- **Rejeição é sinal:** as objeções das personas que NÃO compram são o ouro do relatório.
- **Concretude:** exija detalhes de vida na resposta (a peça na mesa da cozinha, o
  caderninho de anotação) — abstração é o que torna focus group de IA inútil.
- **Não superestime:** avise que focus group SUPERESTIMA intenção; o valor é o mapa de
  objeções/ângulos, não o número absoluto de conversão. Não prometa taxa de conversão real.
- **Calibre quando der:** se o usuário tiver dados reais (vendas passadas, pesquisa),
  use pra ancorar as personas — aí o resultado deixa de ser achismo.

## Custo/escala
8-12 subagentes por rodada. Barato e rápido (minutos). Pra decisão de maior risco,
rode 2 rodadas com posicionamentos diferentes e compare os vereditos.
