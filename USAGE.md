<!-- title: The Scientist Usage Guide -->

# Como usar o The Scientist

Guia rápido - não repete o que já está no `README.md` (arquitetura) ou
nos arquivos de cada agente/skill (regras detalhadas).

## O jeito mais simples: automação completa

Se você quer o ciclo inteiro (intake → estrutura → linguagem →
evidência/veredito → relatório final), diga algo como:

> "Rode o pipeline completo no manuscrito em `~/Documentos/.../artigo.md`"
> "Automação completa nesse artigo"
> "Diagnóstico do zero ao fim"

Isso aciona a skill `pipeline-orchestrator`, que chama os 4 agentes em
sequência sozinha e no final pergunta em que formato você quer o
relatório (chat, HTML com gráficos, ou PDF - se houver conversor
disponível na máquina).

## Revisão pontual (sem rodar tudo)

Para algo específico, fale direto, sem precisar da automação completa:

- **"Revisa a Discussão desse artigo"** / **"Confere as citações"** →
  conversa com `scientific-review` diretamente.
- **"Reescreve esse parágrafo, deixa mais natural"** → aciona
  `manuscript-rewriter` (edita o arquivo de verdade, não só sugere).
- **"Isso tá pronto pra submeter? Qual o risco de desk-reject?"** →
  aciona a skill `publication-strategist` (parecer estratégico rápido,
  não a revisão completa em camadas).
- **"Escreve a carta de resposta aos revisores"** → aciona
  `revision-response-composer`.

## O que o sistema vai te perguntar primeiro

Sempre que você trouxer um manuscrito novo, espere responder (uma vez
só, não a cada mensagem):

1. Em que idioma você quer que a conversa aconteça.
2. País dos autores (e se há financiamento a declarar - CAPES ou
   equivalente do país).
3. Onde está o manuscrito, e o periódico-alvo (se já tiver um).
4. Se é a primeira revisão ou uma re-revisão de algo já avaliado antes.

Isso é o `receptionist` fazendo intake - ele não avalia nada do
conteúdo, só recolhe essas informações e repassa adiante.

## Regras que nunca mudam, seja qual for o pedido

- Zero travessão em texto de manuscrito.
- Nenhuma citação entra sem ser verificada de verdade (nunca de
  memória).
- Limitações reais nunca são amaciadas ou escondidas, mesmo se você
  pedir.
- Divulgação de uso de IA sempre completa, mesmo pedindo algo "mínimo".
- Financiamento (CAPES ou equivalente) sempre conferido quando aplicável.

Se algum pedido esbarrar numa dessas regras, o agente vai recusar essa
parte específica e explicar por quê - isso é esperado, não é um bug.

## Onde as coisas ficam

- Relatórios de revisão: `~/Documentos/doctor agente/`.
- O manuscrito em si: fica no projeto dele, nunca é movido para dentro
  da pasta acima.
- Definições dos agentes/skills: `~/.claude/agents/` e
  `~/.claude/skills/` (espelhados neste repositório).

## Se algo não estiver disponível

Antes de prometer um formato/ferramenta (ex. exportar PDF, publicar
HTML), os agentes checam a máquina primeiro - se algo não estiver
instalado, você recebe um aviso claro em vez de uma promessa que não vai
se cumprir.
