---
name: manuscript-rewriter
description: Reescreve de fato um trecho/seção do manuscrito, aplicando de uma vez a arquitetura narrativa (C-C-C, CARS, Posição de Tópico/Ênfase), a redução de maneirismos de escrita por IA, e hedging calibrado - e aplica a mudança no arquivo via Edit, não só sugere. Preserva 100% do conteúdo científico (dados, alegações, limitações, divulgação de IA) - é reescrita de estilo, nunca de substância. Use quando o usuário pedir para "reescrever"/"melhorar o texto"/"deixar mais natural"/"editar de vez" um trecho específico do manuscrito, não uma revisão de mérito científico.
---

# Manuscript Rewriter

Reescreve e **aplica de verdade** a edição num trecho do manuscrito -
diferente das outras skills de estilo (`narrative-architecture`,
`human-natural-language`), que descrevem o que ajustar mas deixam a
aplicação para quem invocou. Esta skill é o passo de execução: pega os
princípios das outras duas, decide a reescrita concreta, e grava no
arquivo.

## Pré-requisito

Só use esta skill se o agente que a invocou tiver a ferramenta `Edit`
disponível (hoje: `revisor-semantico` e `scientific-review`). Se não
tiver, produza a versão reescrita como texto na resposta e diga
explicitamente que não pode aplicar direto no arquivo - nunca finja que
aplicou uma mudança que só existe na conversa.

## Regra fundamental: estilo, nunca substância

- **Nunca mude** o que está sendo alegado, números, dados, limitações
  divulgadas, ou a seção de divulgação de uso de IA. Isso vale mesmo que
  a reescrita "ficasse melhor" mudando um desses - não é sua decisão
  mudar substância.
- Se ao reescrever você perceber que uma frase parece cientificamente
  errada, exagerada, ou contradiz outro trecho, **não conserte
  silenciosamente dentro da reescrita de estilo** - pare, aponte
  separadamente ao usuário como um achado de conteúdo (isso é escopo do
  `scientific-boss`/Camada 3, não desta skill), e só prossiga com a
  parte estilística depois de decidido o que fazer com o conteúdo.
- Todas as regras de rigor do projeto continuam valendo integralmente
  (zero travessão, citações verificadas, financiamento, IA).

## Processo

1. **Leia o trecho-alvo com contexto**: o parágrafo anterior e o
   seguinte também, não só a frase isolada - mudança de estilo precisa
   manter coesão com a vizinhança.
2. **Aplique nesta ordem** (cada uma é o princípio já detalhado na skill
   de origem, não repita aqui, só siga a ordem):
   a. Estrutura do parágrafo/seção - modelo CARS para Introdução, C-C-C
      para qualquer parágrafo, sequência de declarações para Resultados
      (`narrative-architecture`).
   b. Clareza de frase - Posição de Tópico/Posição de Ênfase, separação
      sujeito-verbo (`narrative-architecture`).
   c. Redução de maneirismos de IA - vocabulário-gatilho, conectores
      formulaicos, burstiness, regra dos três (`human-natural-language`).
   d. Hedging calibrado e micro-edição de frase, se o texto for em
      inglês (`narrative-architecture`).
3. **Mudanças grandes (reescrita de parágrafo inteiro ou mais)**: mostre
   antes/depois ao usuário e peça confirmação antes de aplicar.
   **Mudanças pontuais** (uma frase, reordenar uma cláusula, trocar uma
   palavra-gatilho): pode aplicar direto e reportar depois - não
   precisa de confirmação prévia para cada micro-ajuste.
4. **Aplique via `Edit`**.
5. **Rode as checagens automáticas** de `scientific-review.md` no trecho
   editado (zero travessões, sem placeholder esquecido) antes de
   reportar como concluído.
6. **Resuma o que mudou e por quê**, referenciando qual princípio
   motivou cada mudança (ex. "movida a informação nova para a posição de
   ênfase no final da frase" ou "substituído 'delve into' por verbo mais
   direto") - nunca só "melhorei a frase" sem dizer o que mudou.

## Limites

- Não decide se uma alegação científica está certa/sustentada pelos
  dados - isso é `scientific-boss` (Camada 3).
- Não reclassifica tipo/estrutura do artigo - isso é `research-design`.
- É reescrita de texto **já existente** - nunca inventa conteúdo novo,
  nunca adiciona resultado/dado/citação que não estava no trecho
  original (uma citação nova só entra se o usuário pedir explicitamente
  e ela for verificada, nunca por iniciativa própria da reescrita de
  estilo).
- Fora do pipeline completo, pode ser usada como atalho rápido - o
  usuário aponta um trecho, você aplica isto direto, sem precisar
  acionar `research-design`/`scientific-boss` para uma correção
  pontual de estilo.
