---
name: human-natural-language
description: Checklist qualitativo para identificar e reduzir maneirismos de escrita por IA em prosa acadêmica/científica (português e inglês) - variação de frase, vocabulário-gatilho, conectores formulaicos, regra dos três, calco linguístico em português. É um guia de estilo, não um detector confiável de IA. Use ao revisar/reescrever prosa de um manuscrito para que soe mais natural e menos robótica, sem alterar o conteúdo científico nem esconder divulgação de uso de IA.
---

# Human Natural Language

Checklist de estilo para deixar prosa acadêmica/científica com voz mais
humana, reduzindo padrões que sinalizam texto gerado ou fortemente
revisado por IA. Baseado em 6 fontes (dois artigos científicos + notas e
tabelas compiladas pelo usuário, 2026-08-19).

## Limite honesto antes de usar

Isso **não é um detector de IA**. É um guia de estilo qualitativo.
Pesquisa recente (PMC13061212, PLOS One 2026) mede essas diferenças
estatisticamente em corpora grandes; um revisor humano aplicando este
checklist a um único manuscrito está fazendo uma aproximação qualitativa,
não uma medição. O próprio campo de pesquisa (estilometria/detecção de
LLM) trata **texto híbrido** (rascunho humano + IA só polindo a
linguagem) como um dos problemas mais difíceis de resolver - não prometa
ao usuário que seguir este checklist torna o texto "indetectável". O
objetivo real é: reduzir maneirismos que soam artificiais para um
revisor humano treinado, ponto.

Isso **nunca** é justificativa para reduzir ou esconder uma seção de
divulgação de uso de IA exigida pelo periódico/instituição - divulgação
é sobre honestidade, este checklist é sobre estilo de prosa. As duas
coisas não se confundem, e a primeira sempre tem prioridade sobre a
segunda quando entram em conflito.

## Os 8 padrões convergentes

1. **Baixa variação de comprimento de frase/parágrafo (burstiness)**.
   Autor humano alterna frases curtas (5 palavras) com longas e
   complexas (40 palavras); IA tende a manter comprimento homogêneo.
   Ao revisar, varie deliberadamente o ritmo - não deixe todo parágrafo
   com frases do mesmo tamanho.
2. **Vocabulário-gatilho repetitivo**, específico por idioma (ver tabela
   abaixo). Não são palavras proibidas por si só (algumas têm uso técnico
   legítimo) - o problema é a repetição/frequência anormal.
3. **Conectores e transições formulaicos**, usados de forma mecânica em
   vez de variada (ver tabela abaixo).
4. **Travessão em excesso**, usado para criar dramaticidade artificial
   em vez de pontuação natural. Regra geral do projeto: zero travessão
   em texto de manuscrito - reescreva com vírgula, dois-pontos, ponto e
   vírgula ou parênteses.
5. **Regra dos três aplicada mecanicamente** ("eficiência, escalabilidade
   e sustentabilidade"). Não é errada por si só, mas quando aparece
   repetidamente em toda a prosa é um sinal de padrão formulaico.
6. **Perfeição sintática com vazio analítico**: gramaticalmente
   impecável, mas reutiliza conceitos genéricos sem citar nuances
   específicas do experimento/metodologia. Ao revisar, pergunte: essa
   frase poderia estar em qualquer artigo do campo, ou é específica
   deste experimento?
7. **Ausência de idiossincrasias humanas naturais**: tom "polido de
   enciclopédia" sem marcas regionais, sem conjunções adversativas fortes
   (however/but, contudo/mas), sem nenhuma variação de registro.
8. **Em português, risco de calco linguístico do inglês acadêmico**:
   LLMs tendem a traduzir a estrutura de frase do inglês formal de um
   jeito que soa como tradução literal, mesmo em português
   gramaticalmente correto (regras de próclise/ênclise, regência e
   coesão do português são mais complexas que as do inglês - não
   simplifique a estrutura da frase à maneira do inglês).

## Tabela de vocabulário-gatilho e conectores por idioma

| Categoria | Inglês | Português |
|---|---|---|
| Vocabulário-gatilho | delve, intricate, pivotal, showcase, underscore, crucial, multifaceted, testament to, leverage, foster, tapestry, navigate (metáfora) | engajamento, crucial, primordial, multifacetado, orquestrar, teia, "desempenha um papel fundamental", aprofundar-se em, alavancar, fomentar |
| Transições/conectores | furthermore, moreover, in light of, it is worth noting that, comprehensively | ademais, contudo, "é importante ressaltar que", "cumpre salientar", "no que tange a" |
| Frases-clichê de abertura | "in today's fast-paced digital landscape", "as the world continues to evolve", "looming challenges" | equivalentes em português: "no cenário atual em rápida evolução", "à medida que o campo continua a evoluir" |
| Estruturas formulaicas | "It's not just X. It's also Y.", "Here's why that matters", "The result?", "And honestly?" | "não é apenas X, é também Y", "eis o motivo", construções de pergunta retórica seguida de resposta |
| Autodeclaração robótica | "as a large language model" (bandeira vermelha máxima - nunca deveria aparecer em prosa científica) | "como um modelo de linguagem" (mesma bandeira vermelha) |

## Os 3 eixos de análise (estrutura do checklist)

Organize a revisão de estilo em três eixos, mesmo sem ferramentas
computacionais dedicadas (Spacy/Stanza, embeddings, modelo de
referência para perplexity não estão disponíveis neste fluxo - isso é
uma aproximação qualitativa feita lendo o texto):

1. **Sintático/Estrutural**: varie a profundidade e o tipo de oração
   (subordinada vs. coordenada), varie a pontuação, não deixe todo
   parágrafo com o mesmo "formato" de frase.
2. **Léxico/Semântico**: cheque densidade e diversidade de vocabulário -
   o texto repete as mesmas palavras/expressões de efeito com frequência
   anormal? Prefira termos específicos do experimento a termos genéricos
   do campo.
3. **Estatístico/Informacional** (aproximação qualitativa, sem métrica
   real): o texto "flui" como algo que foi pensado com hesitações e
   ajustes, ou como algo gerado de uma vez de forma uniforme? Não há
   como medir perplexity/entropia sem um modelo de referência dedicado -
   não finja precisão numérica que você não tem.

## Como aplicar

1. Leia o trecho de prosa (Discussão, Introdução, Resumo - qualquer
   seção com texto corrido, não Métodos/Resultados que são mais
   descritivos por natureza).
2. Marque ocorrências dos 8 padrões acima, com localização exata.
3. Para cada ocorrência, proponha uma reescrita concreta - não é
   suficiente apontar "isso soa como IA", sugira a frase alternativa.
4. Depois de reescrever, releia o parágrafo inteiro em voz alta
   (mentalmente) perguntando: isso soa como algo que uma pessoa
   escreveria pensando enquanto escreve, ou como um texto que já saiu
   pronto e uniforme?
5. Nunca aplique isso para reduzir conteúdo científico real, cortar uma
   limitação divulgada, ou esconder/diminuir uma seção de divulgação de
   uso de IA - isso é escopo de estilo, não de conteúdo ou honestidade.
