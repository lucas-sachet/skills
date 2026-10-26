---
name: fazer-questionario
description: Transforma uma decisão que você não consegue tomar sozinho num questionário para outra pessoa responder (um contador, um fornecedor, um sócio, um cliente).
disable-model-invocation: true
---

Transforme algo que o usuário não consegue resolver sozinho num **questionário**: um documento Markdown que ele entrega a uma pessoa para responder quando puder, ou para preencherem juntos numa reunião. Quem recebe tem um conhecimento que o usuário não tem, e o questionário tira isso dela.

**Questione o envio, não o assunto.** Entreviste o usuário apenas sobre o _envio_, que ele sempre sabe responder: para quem vai e o que ele precisa receber de volta. As perguntas do documento miram a **lacuna** entre o que a pessoa sabe e o que o usuário precisa saber.

1. **Para quem vai?** Pergunte, de uma vez, a função da pessoa, o quanto ela entende do assunto e a relação dela com o usuário. Isso define o tom do questionário e quanto contexto ele precisa trazer. Está pronto quando você sabe quem é o destinatário e o que ele sabe que o usuário não sabe.

2. **O que você precisa receber de volta?** Pergunte, de uma vez, as decisões ou informações que o usuário não consegue resolver sozinho e precisa dessa pessoa. Está pronto quando você tem uma lista concreta do que o usuário precisa conseguir decidir ou fazer depois.

3. **Escreva o questionário.** Redija perguntas que mirem a lacuna dos passos 1 e 2, seguindo a estrutura abaixo. Salve em `questionario-<assunto>.md` na pasta atual e diga o caminho. Está pronto quando o arquivo existe e cada item citado no passo 2 é coberto por uma pergunta.

## Estrutura do documento

Trate o documento como um **questionário de descoberta**: o usuário não tem o contexto, o destinatário tem. Ponha as perguntas mais importantes primeiro, porque por escrito talvez só haja uma chance de resposta, e agrupe por tema com títulos `##` quando houver mais do que meia dúzia. Use o modelo abaixo.

<modelo-de-questionario>

# <Título do questionário>

**Objetivo:** por que este questionário existe e qual decisão depende dele.

**De:** <o usuário>, **Para:** <o destinatário>, **Como suas respostas serão usadas:** <onde vão parar>

## Contexto

Um parágrafo que situa quem não estava na cabeça do usuário. O suficiente para responder bem, não uma página.

## Como responder

Prazo e esforço aproximado. Respostas parciais e "não sei" ajudam: avise o que não tiver certeza em vez de pular.

## <Título do tema>

Uma seção `##` por tema. Embaixo, as perguntas, da mais importante para a menos. Cada pergunta trata de uma ideia só, nunca duas juntas, com um espaço para resposta logo abaixo, e uma linha _por que isso importa_ apenas quando a pergunta puder ser mal entendida ou convidar uma resposta apressada.

<exemplo-de-pergunta>
### Quantos pedidos por mês a loja deve ter nos primeiros seis meses?

_Por que isso importa: define se contratamos um sistema de estoque agora ou só depois._

>
</exemplo-de-pergunta>

## Mais alguma coisa?

Um fecho aberto: algo que não perguntamos e que deveríamos saber?

</modelo-de-questionario>
