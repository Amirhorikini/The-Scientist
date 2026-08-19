---
name: statistical-reporting-standards
description: Checklist detalhado de relato estatístico (padrão APA 7ª edição) - checklist universal (descritivas, effect size, IC, poder estatístico, dados faltantes, testagem de pressupostos), checklists por método (t-test, ANOVA, regressão, SEM, HLM, qui-quadrado, não-paramétricos), formatação APA de números/símbolos, red flags de p-hacking/HARKing/GRIM/GRIMMER, e rubrica de pontuação de completude estatística. Use na Camada 3 (Evidência) ao avaliar a seção de Métodos/Resultados de um manuscrito quantitativo - aprofunda o Checklist MFE do scientific-review.
---

# Statistical Reporting Standards

Checklist operacional para avaliar se o relato estatístico de um
manuscrito quantitativo está completo e correto, no padrão APA 7ª
edição. Aprofunda o Checklist MFE do `scientific-review` - use esta
skill quando precisar de rigor estatístico linha por linha, não só a
checagem geral de "a estatística parece adequada?".

## 1. Checklist universal (todo artigo quantitativo)

- **Descritivas**: média (*M*) e desvio-padrão (*SD*) sempre juntos
  (nunca *SD* trocado por erro-padrão *SE* sem dizer); *N* total e por
  grupo; range ou IQR; frequência (*f*) e porcentagem para categóricas -
  nunca só a porcentagem.
- **Effect size (obrigatório pela APA 7ª ed.)**: todo teste estatístico
  precisa vir acompanhado de effect size, não só *p*-valor. Métrica por
  método: *t*-test → Cohen's *d* (pequeno/médio/grande: 0.2/0.5/0.8);
  ANOVA → eta²/eta² parcial (.01/.06/.14); correlação → *r*
  (.10/.30/.50); regressão → R²/*f*² (*f*²: .02/.15/.35); qui-quadrado →
  Cramer's *V*/*phi* (.10/.30/.50); odds ratio → OR (1.5/2.5/4.3). O
  número sozinho não basta - precisa da interpretação de magnitude.
- **Intervalo de confiança**: todo effect size e estimativa-chave deveria
  reportar IC 95% no formato `[limite inferior, limite superior]`;
  interprete o que o IC diz sobre precisão, não só se cruza zero.
- **Significância estatística**: *p*-valor exato (`p = .032`, não só
  `p < .05`); `p < .001` só quando muito pequeno, nunca `p = .000`; nível
  alpha declarado a priori; correção para comparações múltiplas
  (Bonferroni/Holm/FDR); resultados não-significativos relatados
  integralmente, nunca escondidos.
- **Poder estatístico**: análise de poder a priori (meta >= .80, effect
  size assumido, alpha, N necessário), fonte do effect size assumido,
  ferramenta usada (G*Power, pacote `pwr` etc.); para resultados
  não-significativos, discutir risco de erro Tipo II.
- **Dados faltantes**: quantidade e proporção por variável; mecanismo
  discutido (MCAR/MAR/MNAR, não presumido); método declarado (listwise/
  pairwise/imputação múltipla/FIML); idealmente análise de
  sensibilidade comparando métodos.
- **Testagem de pressupostos**: normalidade (Shapiro-Wilk/K-S/Q-Q),
  homogeneidade de variância (Levene), linearidade, independência
  (Durbin-Watson ou justificativa do desenho), multicolinearidade (VIF),
  normalidade/homoscedasticidade de resíduos (regressão) - "N > 30
  então não preciso testar" não é justificativa válida.

## 2. Checklists por método (aplique o que for relevante ao desenho)

- **t-test**: estatística `t(df) = X.XX, p = .XXX`; independente vs.
  pareado correto; Cohen's *d* (ou *d_z* pareado); pressupostos
  testados; correção de Welch se variâncias desiguais; direcionalidade
  (uni/bicaudal) justificada a priori.
- **ANOVA**: `F(df1,df2) = X.XX, p = .XXX`; eta²/eta² parcial/omega²;
  post-hoc quando efeito principal é significativo (Tukey/Bonferroni/
  Games-Howell); interações interpretadas em desenho fatorial;
  esfericidade (Mauchly + correção Greenhouse-Geisser/Huynh-Feldt) em
  medidas repetidas.
- **Regressão linear**: R²/R² ajustado/teste F do modelo; tabela de
  coeficientes completa (*B*, *SE*, *beta*, *t*, *p*, IC 95%); VIF;
  diagnóstico de resíduos (normalidade, homoscedasticidade, outliers via
  Cook's D); método de seleção de variáveis justificado.
- **Regressão logística**: ajuste do modelo (Hosmer-Lemeshow/-2LL/
  Nagelkerke R²); coeficientes (*B*, *SE*, Wald, OR, IC 95% do OR);
  acurácia de classificação/sensibilidade/especificidade/AUC; regra
  EPV (10-20 eventos por preditor).
- **SEM**: N >= 200 (ou 5-10x parâmetros estimados); **pelo menos 4**
  índices de ajuste simultâneos (CFI/TLI >= .95 bom, >= .90 aceitável;
  RMSEA <= .06 bom com IC 90%; SRMR <= .08; qui²/df <= 3); cargas
  fatoriais padronizadas >= .50; CFA antes de SEM (abordagem em duas
  etapas); confiabilidade/validade (CR >= .70, AVE >= .50).
- **Qui-quadrado**: `chi²(df, N=XX) = X.XX, p = .XXX`; Cramer's V (>2x2)
  ou phi (2x2); frequência esperada >= 5 em toda célula (senão, teste
  exato de Fisher); resíduos padronizados quando significativo.
- **Não-paramétricos**: justificativa explícita de por que não usar o
  teste paramétrico; teste correto (Mann-Whitney/Wilcoxon/Kruskal-
  Wallis/Friedman); effect size (*r* = Z/√N para Mann-Whitney).

## 3. Formatação APA 7ª edição (números e símbolos)

- Sem zero à esquerda em estatísticas que não passam de 1.0 (`r = .45`,
  não `r = 0.45`) - vale para *r*, *R*, proporções/p-valor, Cramer's V,
  phi, eta², R², beta padronizado.
- Com zero à esquerda em estatísticas que podem passar de 1.0 (`M =
  0.75`) - vale para M, SD, B, Cohen's d, t, F, chi².
- Duas casas decimais geralmente; p-valor com 2-3 casas (`p = .032`,
  nunca `p = .0321`); porcentagem com 0-1 casa decimal.
- Itálico: *M*, *SD*, *SE*, *N*/*n*, *t*, *F*, *p*, *r*, *R*, *z*, *d*,
  *B*, *beta*, *chi²*. Sem itálico: df, SS, MS, OR, CI, VIF, AIC, BIC,
  CFI, TLI, RMSEA, SRMR, ICC.
- Tabela de três linhas (acima do cabeçalho, abaixo do cabeçalho, fim da
  tabela) - sem linhas verticais; números alinhados à direita,
  decimais alinhados.

## 4. Red flags estatísticos (sinais de alerta, não veredito automático)

Estes são gatilhos para investigar mais, não uma condenação automática -
mas quando confirmados, viram achado real no relatório.

- **P-hacking**: muitos *p* concentrados em .04-.05; relato seletivo
  (só resultados significativos aparecem); estratégia de análise não
  declarada a priori; subgrupos post-hoc "descobertos"; tamanho de
  amostra flexível sem regra de parada; exclusão de outliers em massa
  sem critério claro.
- **HARKing** (hipotetizar depois de ver o resultado): hipóteses 100%
  confirmadas sem exceção; revisão de literatura claramente construída
  post-hoc; mudança de direção da hipótese sem reconhecer.
- **Effect size/IC ausentes**: conclusão baseada só em p-valor; IC
  ausente ou extremamente largo; effect size relatado inconsistente com
  o que os dados brutos permitiriam calcular.
- **Amostra**: sem análise de poder; N < 10x preditores em regressão;
  atrito de amostra grande e não explicado.
- **Comparações múltiplas sem correção**: múltiplos t-tests em vez de
  ANOVA para 3+ grupos; múltiplas variáveis dependentes testadas
  separadamente sem Bonferroni/FDR; testar vários modelos e reportar só
  "o melhor".
- **Pressupostos**: testagem ausente; violação relatada mas análise
  original mantida mesmo assim; VIF alto (>10) sem ação.
- **Sinais de inconsistência numérica** (nível mais sério, pode indicar
  erro ou fabricação, não só relato incompleto):
  - **GRIM**: para dados de escala discreta, a média relatada precisa
    ser algebricamente alcançável dado o N e a precisão declarados - se
    não for, é um sinal real de inconsistência (Brown & Heathers, 2017).
  - **GRIMMER**: extensão do GRIM para desvio-padrão - mesmo princípio,
    checando se o SD relatado é alcançável dado a média e N.
  - `p` incompatível com a estatística/df relatados (não bate com
    nenhuma leitura de cauda plausível).
  - df inconsistente com o N relatado no texto.
  Estes quatro só devem ser levantados quando você (ou o usuário)
  consegue de fato recalcular e checar - nunca alegue "GRIM
  inconsistente" por intuição sem fazer a conta.

## 5. Rubrica de completude do relato estatístico (0-100)

| Dimensão | Peso | Critério de nota máxima |
|---|---|---|
| Descritivas completas | 15% | M, SD, N, range presentes |
| Effect size relatado | 20% | Todo teste acompanhado de effect size |
| Intervalo de confiança | 15% | Estimativas-chave com IC |
| Testagem de pressupostos | 15% | Todos os pressupostos relevantes testados |
| Poder estatístico | 10% | Análise de poder a priori completa |
| Dados faltantes | 10% | Quantidade + método de tratamento relatados |
| Formatação APA | 10% | Símbolos, decimais, tabelas conformes |
| Ausência de red flags | 5% | Nenhum red flag da seção 4 detectado |

Faixas: 90-100 exemplar; 70-89 adequado (omissões menores); 50-69
precisa melhorar (omissões significativas); 30-49 inadequado; 0-29
insuficiente para sustentar as conclusões.

## 6. Ordem de checagem recomendada

1. A pergunta de pesquisa corresponde ao método de análise escolhido?
2. Testagem de pressupostos está relatada?
3. Checklist universal (seção 1), item por item.
4. Checklist específico do método (seção 2).
5. Varredura de red flags (seção 4).
6. Formatação APA (seção 3).
7. Pontuação de completude (seção 5).

## Relação com o resto do pipeline

Use esta skill no `scientific-boss` (Camada 3 - Evidência), como
aprofundamento do Checklist MFE já existente - o Checklist MFE cobre
metodologia/figuras de forma mais ampla, esta skill cobre relato
estatístico linha por linha. Não substitui as regras de rigor
(travessão, citações, limitações, financiamento, IA) nem o Princípio da
Integridade do Dado - complementa especificamente a checagem numérica.
