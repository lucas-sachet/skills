---
name: montar-plano
description: 'Transforma a conversa atual num plano escrito (objetivo, decisões, passos, riscos), sem entrevistar o usuário: só reúne o que já foi combinado.'
disable-model-invocation: true
---

Esta skill pega o que já foi dito na conversa e produz um **plano** por escrito. NÃO entreviste o usuário: apenas sintetize o que você já sabe. Se faltar algo essencial, anote em "Perguntas em aberto" em vez de perguntar agora.

## Processo

1. **Reúna o contexto.** Releia a conversa e, se o usuário apontou arquivos (planilhas, contratos, propostas), leia-os. Use as palavras do próprio usuário para chamar as coisas (produtos, clientes, setores), sem inventar termos.

2. **Escreva o plano** com o modelo abaixo e salve em `plano-<assunto>.md` na pasta atual.

3. **Mostre e confirme.** Diga onde o arquivo ficou, resuma o plano em poucas linhas e pergunte se algo importante ficou de fora ou foi entendido errado.

<modelo-de-plano>

# Plano: <nome do projeto>

## Situação e problema

O que está acontecendo hoje e qual problema (ou oportunidade) isto resolve, do ponto de vista de quem sofre com ele (o cliente, a equipe, o dono).

## Objetivo

O resultado que queremos alcançar, em uma ou duas frases, de forma que dê para dizer depois se foi alcançado ou não.

## Como saberemos que deu certo

Lista de sinais concretos e mensuráveis (por exemplo: "responder todo orçamento em até 24 horas", "reduzir devoluções de 8% para 4% em três meses").

## Para quem

Quem é afetado ou beneficiado: clientes, equipe, fornecedores, sócios. Para cada grupo, o que muda na prática. Escreva como uma lista longa e numerada, no formato:

1. Como <quem>, quero <o quê>, para <benefício>

<exemplo>
1. Como cliente, quero receber o orçamento no mesmo dia, para decidir sem ter que cobrar a loja.
</exemplo>

## Decisões tomadas

As escolhas já feitas e o motivo de cada uma: o que será feito, por quem, com que ferramentas, em que ordem, com que orçamento e prazo. Registre a decisão e o porquê, não detalhes que mudam rápido (como preços de hoje ou nomes de planilhas).

## Passos principais

As grandes etapas em ordem, sem entrar em detalhes de tarefa (para isso existe `/dividir-em-tarefas`).

## Riscos e dependências

O que pode dar errado, o que depende de terceiros e o que fazer se acontecer.

## Fora do escopo

O que este plano deliberadamente NÃO cobre.

## Perguntas em aberto

O que ainda precisa ser decidido ou descoberto, e quem pode responder.

## Notas

Qualquer outra informação útil.

</modelo-de-plano>
