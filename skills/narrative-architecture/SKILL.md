---
name: narrative-architecture
description: Arquitetura narrativa e clareza de frase para manuscritos científicos - o framework Contexto-Conteúdo-Conclusão (C-C-C) aplicado em todo nível (frase, parágrafo, seção, artigo inteiro), o Modelo CARS de Swales para a Introdução (Território/Nicho/Ocupação do Nicho), a sequência de declarações para Resultados, os princípios de Posição de Tópico/Posição de Ênfase/Separação Sujeito-Verbo (Gopen & Swan) para clareza de frase na primeira leitura, coesão lexical (Halliday & Hasan) como alternativa a conectores mecânicos, e micro-edição de inglês acadêmico (posição de advérbio, adensamento nominal, hedging calibrado). Use ao revisar/reescrever a narrativa de um manuscrito (Introdução, Resultados, Discussão) ou quando o usuário quiser transformar dados em uma história coerente.
---

# Narrative Architecture

Ferramentas para dar a um manuscrito científico um arco narrativo
coerente (Problema → Lacuna → Solução → Implicação) e frases que um
revisor entende na primeira leitura, sem precisar reler. Baseado em
Mensh & Kording (2017, PLOS Computational Biology) e Gopen & Swan (1990,
American Scientist) - ver `REFERENCES.md` do projeto.

## O framework Contexto-Conteúdo-Conclusão (C-C-C)

Todo bom trecho de escrita científica, em qualquer escala, segue o
mesmo padrão de três partes - e evita as duas perguntas frustradas do
leitor: "por que você está me contando isso?" (contexto ausente) e "e
daí?" (conclusão ausente).

| Nível | Contexto | Conteúdo | Conclusão |
|---|---|---|---|
| Sentença | Define o tópico | Dados/ideia nova | Conclusão memorável |
| Parágrafo | Primeira frase: tópico | Corpo: ideia nova | Última frase: fecha com conclusão |
| Seção | Introdução: lacuna | Resultados: dados | Discussão: significância |
| Artigo inteiro | Introdução | Resultados | Discussão |

Isso mapeia diretamente no arco narrativo Problema → Lacuna → Solução →
Implicação: Problema/Lacuna = Contexto, Solução/Resultados = Conteúdo,
Implicação = Conclusão. Um manuscrito sem essa correspondência clara em
cada nível está estruturalmente fraco, mesmo que os dados sejam sólidos.

**Erro comum a sinalizar**: estrutura cronológica que segue o processo
de pesquisa real ("primeiro tentamos X, não funcionou, então tentamos
Y..."). Revisores se importam com a alegação final, não com o caminho
autobiográfico até ela - isso também é coberto pela regra de rigor
existente de "metodologia como narrativa limpa, não log de depuração".

## Alinhamento do Gap de Pesquisa (Modelo CARS de Swales)

A Introdução deve progredir por parágrafos cada vez mais específicos até
expor exatamente a lacuna que o artigo preenche. Isso tem nome formal na
linguística de gênero acadêmico: o **modelo CARS** (*Create a Research
Space*) de Swales (1990), usado como padrão-ouro por editores para
avaliar se uma Introdução tem a estrutura narrativa correta - três
"movimentos" (moves), cada um com passos internos:

1. **Move 1 - Estabelecer o Território**: reivindicar centralidade do
   tema (por que ele importa), fazer generalizações sobre o estado do
   campo, revisar a literatura relevante. Corresponde ao(s) parágrafo(s)
   inicial(is) - por que o tema amplo importa, e o que o campo como um
   todo ainda não resolveu (lacuna de campo).
2. **Move 2 - Estabelecer o Nicho**: argumentar que existe uma lacuna
   útil na literatura atual - por quatro vias possíveis: contra-alegação
   (contestar um achado prévio), indicação de lacuna, levantamento de
   pergunta, ou continuação de uma tradição de pesquisa. Corresponde
   ao(s) parágrafo(s) intermediário(s) - o que é desconhecido
   especificamente sobre o subtema do estudo (lacuna de subcampo).
3. **Move 3 - Ocupar o Nicho**: delinear o propósito do trabalho,
   anunciar a pesquisa presente, anunciar os achados principais (opcional
   em algumas áreas), indicar a estrutura do artigo. Corresponde ao
   último parágrafo antes do objetivo - a lacuna específica e testável
   que este estudo endereça, e uma prévia compacta de como os resultados
   a preenchem.

Cada parágrafo do Move 1/2 segue o mesmo micro-padrão: frase de
orientação (contexto) → o que a literatura já mostrou (conhecido) →
frase final que expõe o que falta (desconhecido, a lacuna). Se um
parágrafo da Introdução não termina apontando uma lacuna real, ele
provavelmente não deveria estar lá, ou está mal cortado.

**Teste prático**: consiga articular em uma frase "a literatura sabe X,
mas não sabe Y, e isso importa porque Z" - se você não consegue
completar essa frase com o que está na Introdução do manuscrito, a
lacuna não está clara o suficiente para o leitor. Ao revisar, identifique
explicitamente em qual Move cada parágrafo da Introdução está e se a
progressão 1→2→3 está completa - uma Introdução que pula direto de Move
1 para Move 3 (sem estabelecer o nicho) é a falha mais comum.

## Resultados como sequência de declarações

Cada parágrafo/subseção de Resultados deve responder a uma pergunta
implícita, não só narrar o que foi feito:

- **Frase inicial**: formula a pergunta que o parágrafo responde ("Para
  verificar que...", "Para determinar se...", "Em seguida, testamos...").
- **Meio**: dados e lógica relevantes.
- **Frase final**: responde diretamente à pergunta posta na primeira
  frase.

Títulos de figura devem comunicar a **conclusão** da análise, não só
descrever o que está mostrado; a legenda é quem explica a metodologia.
Isso é relevante porque parte dos leitores pula da Introdução direto
para as figuras.

## Evitar zig-zag, usar paralelismo

- Toque em cada ideia central uma única vez, num único lugar - não
  espalhe o mesmo argumento em pontos não-consecutivos do texto.
- Agrupe frases/parágrafos relacionados; ideias similares devem ficar
  consecutivas.
- Se há múltiplas razões paralelas para uma interpretação, comunique-as
  com a mesma estrutura sintática (ex. sempre "X aumenta Y", não
  misturar com "há um aumento de Y causado por X") - variar a forma para
  a mesma função confunde o leitor sobre se são conceitos diferentes.

## Clareza de frase: Posição de Tópico e Posição de Ênfase

Princípio central de Gopen & Swan, resumido em uma frase: **"Coloque na
posição de tópico a informação antiga que conecta para trás; coloque na
posição de ênfase a informação nova que você quer que o leitor
enfatize."**

- **Posição de tópico** (início da frase): é onde o leitor busca
  contexto e conexão com o que já foi dito. Informação "velha"
  (já mencionada) deve aparecer aqui - não informação nova. Uma frase
  cujo início não conecta com o que veio antes quebra o fio da leitura.
- **Posição de ênfase** (final da frase, ou antes de dois-pontos/
  ponto-e-vírgula): é onde o leitor naturalmente deposita mais atenção -
  o equivalente do "salve o melhor para o final". Informação nova e
  importante deve aparecer aqui, não em algum lugar perdido no meio da
  frase.
- **Separação sujeito-verbo**: o leitor espera que o verbo venha logo
  depois do sujeito. Material longo intercalado entre os dois é lido
  como interrupção de menor importância, mesmo quando o autor pretendia
  que fosse importante - se uma informação merece destaque, ela precisa
  estar na posição de ênfase, nunca escondida entre sujeito e verbo.
- **Uma frase é longa demais não por contagem de palavras**, mas quando
  tem mais candidatos a "informação que merece ênfase" do que posições
  de ênfase disponíveis. Frases de 100 palavras bem estruturadas se leem
  com facilidade; frases de 20 palavras mal estruturadas, não.

**Como aplicar numa revisão**: para cada frase problemática, identifique
(1) o que é informação já conhecida pelo leitor a essa altura - deve
estar no início; (2) o que é a informação nova/importante desta frase -
deve estar no final; (3) se sujeito e verbo estão separados por mais de
uma cláusula curta, mova o material intercalado para outro lugar (início
da próxima frase, ou uma frase própria) em vez de deixá-lo preso no
meio.

## Micro-edição de nível de frase (inglês acadêmico nativo)

Técnicas pontuais para prosa em inglês soar como a de um autor nativo
experiente, sem exagero retórico. Aplicáveis principalmente a manuscritos
escritos ou traduzidos para inglês (o caso comum de submissão
internacional):

- **Coesão lexical em vez de conectores mecânicos** (Halliday & Hasan,
  1976): a coesão de um texto vem de dois tipos - coesão gramatical (uso
  de conectores como "furthermore"/"moreover"/"ademais") e coesão
  **lexical** (o fluxo natural de ideias por repetição controlada,
  sinônimos e cadeias semânticas). Textos que dependem só do primeiro
  tipo soam mecânicos. Em vez de abrir toda frase nova com um conector
  formal, embuta a transição no próprio sujeito da frase ou na estrutura
  sintática - ex., ao invés de "Furthermore, the results indicate...",
  prefira retomar o sujeito anterior diretamente ("These results also
  indicate...", ou simplesmente conectar pela repetição do termo-chave).
- **Posição de advérbios em verbos compostos**: reposicione advérbios
  para o meio do verbo composto em vez do início/fim da frase - "is
  currently poorly understood" em vez de "currently, we understand this
  poorly". Isso é convenção do inglês acadêmico formal, não estilo
  pessoal.
- **Adensamento nominal e cláusulas com particípio presente**: converta
  frases prolixas em grupos nominais densos, e use cláusulas com "-ing"
  para amarrar uma consequência à frase anterior sem precisar de um
  conector novo - ex. "..., thereby reducing X" ou "..., paving the way
  for Y" no lugar de uma frase nova começando com "This reduces X" ou
  "This opens the way for Y".
- **Hedging técnico calibrado**: troque verbos absolutos ("proves",
  "shows", "demonstrates" quando o desenho não sustenta certeza total)
  por atenuação apropriada ao que os dados realmente permitem
  ("suggests", "is consistent with", "strongly points toward"). Isto
  **não é** a mesma coisa que a regra de rigor de "não empilhar hedge nas
  Limitações" - aqui o objetivo é calibrar o verbo à força real da
  evidência uma vez, não amaciar repetidamente a mesma ressalva. Uma
  alegação sustentada por dado forte pode e deve usar verbo mais direto;
  o erro a corrigir é o oposto, verbo absoluto para evidência
  moderada/correlacional.
- **Princípio do peso final (End-Weight)**: mesma ideia da Posição de
  Ênfase acima (Gopen & Swan) com outro nome - posicione a informação
  mais complexa/de maior carga cognitiva no final da oração, não no
  início. Não é uma técnica adicional, é a mesma regra reaparecendo na
  literatura de estilo em inglês - não tratar como dois princípios
  diferentes.

## Precificação de limitações (framing, não ocultação)

Limitações reais podem ser expostas de um jeito que funciona como gancho
para trabalho futuro, em vez de soar como falha metodológica pura -
isso é uma questão de **enquadramento retórico**, nunca de **omissão ou
suavização de conteúdo**. A regra de rigor do projeto (nunca amaciar ou
remover limitações reais) continua valendo integralmente: o dado, a
limitação em si, e sua honestidade completa não mudam. O que pode mudar
é a frase de fechamento logo depois de declarar a limitação - de um
final sem saída ("isso é uma fraqueza do estudo") para uma ponte
concreta ("estudos futuros com [desenho específico] poderiam resolver
essa lacuna medindo [o quê exatamente]"). Isso só é legítimo quando a
sugestão de trabalho futuro é real e específica - uma ponte vaga
("mais pesquisa é necessária") não conta e é, ela mesma, um dos clichês
listados na skill `human-natural-language`.

## Relação com o resto do pipeline

- Aplicado principalmente pelo `revisor-semantico` na Camada 2
  (Reconstrução), depois de resolver estrutura/redundância, ao trabalhar
  frase a frase.
- O framework C-C-C e o Alinhamento do Gap reforçam e aprofundam a
  "Linha de Coerência Interna" do eixo 4 da skill `publication-strategist`
  - use as duas juntas quando for revisar Introdução/Discussão a fundo.
- Não sobrepõe as regras de rigor científico (travessão, citações,
  limitações, financiamento, IA) - todas continuam valendo
  integralmente por cima de qualquer decisão de arquitetura narrativa.
