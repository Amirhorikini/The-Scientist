---
name: revision-response-composer
description: Compõe a carta de resposta a revisores/editor (formato Comentário do Revisor → Resposta do Autor → Mudança Feita, R→A→C) depois de uma rodada de revisão por pares real ou simulada pelo scientific-boss. Inclui tabela de mudanças página-a-página, forma correta de discordar de um revisor com evidência, e regra de que nenhum comentário pode ficar sem resposta. Use quando o usuário tiver recebido pareceres (reais ou do Modo Banca/Re-revisão do scientific-boss) e precisar escrever a carta de resubmissão.
---

# Revision Response Composer

Monta a carta de resposta formal a revisores/editor depois de uma
rodada de revisão, no formato **R→A→C** (Reviewer comment → Author
response → Changes made) que periódicos esperam.

## Regras inegociáveis

- **Todo comentário recebe resposta - nenhum pode ser pulado**, mesmo os
  menores. Uma lista de fraquezas do parecer é ilimitada; se o
  `scientific-boss` (ou um revisor real) levantou 12 itens, a carta tem
  12 respostas, não um resumo dos "principais".
- **Discordar exige evidência, nunca só "discordamos"**. Ver seção
  "Como discordar corretamente" abaixo.
- **Reconhecimento de pontos fortes só quando o parecer de fato elogiou
  algo** - não fabrique elogio para preencher a seção; se o parecer não
  teve nenhum ponto positivo explícito, pule esse bloco em vez de
  inventar um.
- **Toda mudança precisa de localização exata** (página/parágrafo na
  versão revisada) - "mudamos isso" sem dizer onde é uma resposta fraca
  que obriga o revisor a caçar a alteração.
- Isso é sobre **compor a carta**, não sobre decidir o que mudar - as
  mudanças em si vêm do `revisor-semantico`/`scientific-boss`/decisão do
  usuário; esta skill só formata a resposta de forma completa e
  rastreável.

## Estrutura da carta

```
# Resposta aos Comentários dos Revisores

## Informações do Manuscrito
- Título / ID do manuscrito / Data de submissão original / Data desta
  revisão / Rodada de revisão

## Resumo das Mudanças
[300-500 palavras resumindo as mudanças principais desta rodada]
- Mudanças estruturais (reorganização de seção, contagem de
  palavras antes → depois)
- Conteúdo novo (análises/dados/referências adicionados)

## Resposta ao Revisor/Adequação ao Periódico
### Comentário 1
> [citação direta do comentário]
**Resposta do Autor**: [...]
**Mudança Feita**: [página X, parágrafo Y - o quê exatamente mudou]

## Resposta ao Revisor 1 (Metodologia)
### Pontos Fortes Reconhecidos (só se o parecer citou algo positivo)
### R1-F1, R1-F2... [uma entrada por fraqueza levantada, sem limite de quantidade]
### Perguntas do R1
### Itens Menores do R1 (tabela: # | comentário | ação tomada | localização)

## Resposta ao Revisor 2 (Domínio) / Revisor 3 (Perspectiva) / Advogado do Diabo
[mesmo formato acima para cada persona que gerou achados]

## Resposta às Revisões Obrigatórias (do veredito do scientific-boss)
[tabela: # | revisão exigida | status (Completo/Parcialmente Endereçado) | resumo | localização]

## Log de Mudanças Página-a-Página
[tabela: página original | página revisada | seção | descrição da mudança]

## Encerramento
[agradecimento, afirmação de que a versão revisada endereça as
preocupações levantadas, ou explicação honesta do que não foi
totalmente resolvido e por quê]
```

## Como discordar corretamente

Discordar de um revisor é legítimo e esperado às vezes - mas precisa de
estrutura, não só negação:

**Certo**:
> Revisor: sugere usar o Método X em vez do Método Y.
>
> **Resposta do Autor**: Agradecemos a sugestão. Optamos pelo Método Y
> pelos seguintes motivos: (1) performa melhor para [tipo específico de
> dado] (citação verificada); (2) os pressupostos do Método X (ex.
> [pressuposto]) não são satisfeitos no nosso desenho. Entretanto,
> adicionamos uma checagem de robustez com o Método X no Apêndice B, com
> resultados consistentes.
>
> **Mudança Feita**: Apêndice B (p. 25-26) com a checagem de robustez;
> justificativa da escolha do Método Y na seção de Metodologia (p. 9,
> §3).

**Errado**:
> **Resposta do Autor**: Discordamos. O Método Y é apropriado.

A diferença: a resposta certa dá razão específica, cita evidência
(verificada, nunca de memória - regra de rigor do projeto), e ainda
assim oferece algo ao revisor (a checagem de robustez) em vez de só
negar.

## Características de resposta fraca (evitar)

- **Perfunctória**: "Corrigido" sem dizer o quê.
- **Evasiva**: não responde a pergunta difícil de fato.
- **Defensiva sem explicação**: "o revisor entendeu errado" sem dizer
  por quê.
- **Promete demais**: reconhece todos os problemas mas não oferece
  solução para nenhum.
- **Sem marcador de local**: mudança feita mas sem dizer onde, obrigando
  o revisor a procurar.

## Relação com o resto do pipeline

Use depois que o `scientific-boss` já produziu um veredito (primeira
rodada ou Modo Re-revisão) - a carta consolida a resposta a esse
veredito. Se o manuscrito ainda não foi revisado nenhuma vez, não há o
que responder ainda; rode o pipeline completo primeiro.
