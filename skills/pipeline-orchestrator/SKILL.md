---
name: pipeline-orchestrator
description: Executa o pipeline completo do The Scientist de forma automática e sistemática - dispara receptionist, research-design, revisor-semantico e scientific-boss em sequência, repassando a saída de cada etapa para a próxima, e monta o Relatório de Diagnóstico Final ao término. Use quando o usuário pedir para "rodar todos os agentes", "automação completa", "rodar o pipeline inteiro", ou um "diagnóstico do zero ao fim" sobre um manuscrito - em vez de invocar cada agente manualmente um por um.
---

# Pipeline Orchestrator

Gatilho único para rodar as etapas do **The Scientist** sistematicamente,
sem exigir que o usuário (ou você) invoque cada agente manualmente um a
um. Você (quem invocou esta skill) precisa ter a ferramenta `Agent`
disponível.

## Antes de começar

Confirme que você tem a localização do manuscrito - peça se não tiver.
Não invente um caminho.

Pergunte também, **antes da primeira chamada de agente**, em qual
formato o usuário quer o Relatório de Diagnóstico Final (chat/HTML/PDF -
ver critérios completos em `scientific-review.md` § "Relatório de
Diagnóstico Final", incluindo checar se há conversor de PDF disponível
antes de prometer esse formato). Saber isso desde o início evita ter que
voltar e perguntar depois de já ter rodado tudo.

## Sequência de execução

Execute nesta ordem exata, **uma etapa de cada vez - nunca em
paralelo** (cada etapa depende do resultado completo da anterior):

1. **`receptionist`**: `Agent({subagent_type: "receptionist", prompt: "<caminho do manuscrito, e que o pedido é pipeline completo>"})`.
   Colete o Cartão de Entrada (idioma, país/financiamento, periódico-alvo,
   rodada de revisão). Guarde-o na íntegra - vai ser repassado para
   todas as etapas seguintes.
2. **`research-design`**: `Agent({subagent_type: "research-design", prompt: "<Cartão de Entrada + caminho do manuscrito>"})`.
   Guarde o Relatório de Design completo.
3. **`revisor-semantico`**: `Agent({subagent_type: "revisor-semantico", prompt: "<Cartão de Entrada + Relatório de Design completo>"})`.
   Guarde o Relatório de Linguagem completo.
4. **`scientific-boss`**: `Agent({subagent_type: "scientific-boss", prompt: "<Cartão de Entrada + Relatório de Design + Relatório de Linguagem, ambos completos>"})`.
   Guarde a Carta de Decisão completa.
5. **Relatório de Diagnóstico Final**: monte você mesmo agora, seguindo
   à risca a estrutura já definida em `scientific-review.md` § "Relatório
   de Diagnóstico Final" - resumo executivo, resultado de cada
   checklist, conclusão isolada de cada agente (reproduzida na íntegra,
   nunca fundida numa voz só), gráficos, sugestão de periódico com fator
   de impacto verificado no momento, e plano de ação em 3 níveis
   (Urgente/Intermediário/Leve).

Uma chamada explícita a `scientific-review` como etapa própria é
opcional - o Cartão de Entrada + Relatório de Design já cobrem a
Camada 1; inclua essa chamada só se quiser a leitura diagnóstica
independente dele antes do `research-design`, não é obrigatório para o
pipeline funcionar.

## Regras

- **Nunca invente conteúdo de uma etapa que não rodou de fato.** Se uma
  etapa falhar ou não retornar um relatório completo, pare e avise o
  usuário - não prossiga como se tivesse funcionado, e não preencha a
  lacuna com achados inventados.
- **Preserve os relatórios na íntegra entre etapas** - não resuma o
  Relatório de Design antes de repassar ao `revisor-semantico`, por
  exemplo. Cada etapa precisa do relatório completo da anterior, um
  resumo pode esconder um achado que a próxima etapa precisava saber.
- **Uma falha numa etapa não derruba silenciosamente as outras** - se
  `research-design` não concluir, registre isso explicitamente no
  Relatório de Diagnóstico Final em vez de omitir a seção.
- Todas as regras de rigor do projeto (travessão, citações, limitações,
  financiamento, IA, dado não confiável) continuam valendo em cada
  etapa - esta skill só orquestra a sequência, não substitui nem afrouxa
  nenhuma regra de rigor de nenhum agente.

## Quando NÃO usar

Para uma revisão pontual (só a Discussão, só checar citações, só
reescrever um parágrafo), não acione esta automação - fale direto com
`scientific-review` ou invoque a skill específica (`manuscript-rewriter`,
`narrative-architecture` etc.). Esta skill é para quando o usuário quer
o ciclo completo, do zero ao Relatório de Diagnóstico Final.
