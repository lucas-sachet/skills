---
name: responder-cliente
description: Escreve e-mails e mensagens para clientes (respostas, orçamentos, cobranças, reclamações, follow-up) no tom de voz da empresa, guardado num arquivo que melhora a cada uso. Use quando o usuário colar uma mensagem de cliente, pedir "responde esse cliente", "escreve um e-mail para", "como respondo isso" ou "cobrar um cliente".
---

Escreva mensagens para clientes que soem como a empresa do usuário, não como um robô. O **tom de voz** da empresa fica guardado no arquivo `tom-de-voz.md`, que começa como um rascunho e vai sendo ajustado a cada mensagem até ficar concreto e alinhado.

## Passos

1. **Ache o tom de voz.** Procure `tom-de-voz.md` na pasta atual. Se existir, leia-o inteiro, incluindo o histórico de ajustes. Se não existir, siga [Criar o tom de voz](#criar-o-tom-de-voz) antes de escrever qualquer mensagem.

2. **Entenda a mensagem.** Se o usuário colou a mensagem do cliente, leia e identifique: o que o cliente quer, como ele está se sentindo (com pressa, irritado, em dúvida), e o que precisa ser respondido ponto a ponto. Se o usuário só descreveu a situação, trabalhe com isso. Se faltar um fato que muda a resposta, pergunte em uma única mensagem curta.

3. **Não invente fatos.** Preço, prazo, política de troca, desconto e promessa só entram na mensagem se o usuário informou ou se estão num documento da pasta. Quando faltar, escreva `[CONFIRMAR: ...]` no lugar e avise o usuário na entrega. Nunca prometa compensação, reembolso ou exceção que o usuário não autorizou.

4. **Escreva a mensagem** no tom do arquivo. Regras gerais, a menos que o tom de voz diga o contrário:
   - Responda primeiro o que o cliente perguntou, depois o resto.
   - Uma ação clara no final: o que o cliente deve fazer, ou o que a empresa fará e até quando.
   - Curta o bastante para ser lida no celular.
   - Assunto de e-mail específico ("Seu orçamento da reforma, com prazo"), nunca genérico ("Retorno").

5. **Trate os casos difíceis com um roteiro.**
   - **Reclamação:** reconheça o problema com as palavras do cliente, sem se defender nem culpar ninguém; diga o que será feito e até quando; ofereça um canal direto.
   - **Cobrança:** comece cordial, informe valor e vencimento, facilite o pagamento (como pagar, segunda via) e, nas cobranças seguintes, aumente a firmeza em pequenos degraus, sem ameaçar.
   - **Orçamento ou proposta:** resuma o que está incluído, o valor, a validade e o próximo passo; não deixe o cliente adivinhar como aceitar.
   - **Follow-up:** lembre o contexto em uma frase, traga algo novo ou útil (não apenas "alguma novidade?") e facilite a resposta com uma pergunta de sim ou não.
   - **Dizer não:** diga o não logo, explique o motivo em uma frase e ofereça uma alternativa real.

6. **Entregue e peça ajuste.** Mostre a mensagem pronta, avise o que ficou como `[CONFIRMAR]`, e pergunte: "Ficou com a sua cara? O que você mudaria?". Se o usuário alterar o texto ou pedir mudanças, **atualize o `tom-de-voz.md`** (veja [Ajustar o tom de voz](#ajustar-o-tom-de-voz)).

## Criar o tom de voz

Se não há `tom-de-voz.md`, pergunte tudo de uma vez, em uma única mensagem, e diga que respostas curtas bastam:

- Qual é o negócio e quem são os clientes?
- Como você fala com um cliente: mais formal ou mais próximo? Usa "você", "senhor(a)", o primeiro nome?
- Cole 1 ou 2 mensagens suas de que você gostou e, se tiver, uma de que não gostou.
- Quais palavras ou expressões a empresa usa, e quais evita?
- Como você assina e se despede?
- Usa emojis? Em quais situações?

Com o que vier, crie o arquivo com o modelo abaixo, marcando **Estado: rascunho**. Se o usuário não responder tudo, preencha só o que sabe e liste o resto em "A descobrir". Não invente regras de tom.

<modelo-de-tom-de-voz>

# Tom de voz: <nome da empresa>

**Estado:** rascunho | em ajuste | alinhado
**Última atualização:** <data>

## Quem somos e com quem falamos

O negócio, os clientes e o que eles esperam de nós.

## Como falamos

- Tratamento: ...
- Formalidade: ...
- Tamanho das mensagens: ...
- Emojis: ...

## Palavras e expressões

- Usamos: ...
- Evitamos: ...

## Abertura e despedida

- Abrimos com: ...
- Assinamos: ...

## Exemplos que representam a empresa

> Mensagem de exemplo, com uma nota do porquê é a nossa cara.

## Exemplos que NÃO são a nossa cara

> Mensagem de exemplo, com uma nota do porquê.

## A descobrir

O que ainda não sabemos sobre o jeito de falar da empresa.

## Histórico de ajustes

- <data>: o que mudou e por quê (ex.: "cliente reclamou de frieza, passamos a abrir com o primeiro nome").

</modelo-de-tom-de-voz>

## Ajustar o tom de voz

O arquivo só melhora se for atualizado com o uso. Depois de cada mensagem entregue:

- **O usuário corrigiu o texto?** Compare com o que você escreveu, descubra o padrão (mais curto, menos formal, outra abertura) e registre como regra no arquivo, com a data em "Histórico de ajustes". Uma correção isolada vira nota; a mesma correção duas vezes vira regra.
- **O usuário colou uma mensagem boa dele?** Acrescente em "Exemplos que representam a empresa", com a razão.
- **Surgiu uma dúvida que o arquivo não responde?** Anote em "A descobrir" e pergunte ao usuário na próxima oportunidade.
- **Mude o Estado.** Passe para `em ajuste` quando o usuário já corrigiu pelo menos uma mensagem. Passe para `alinhado` somente quando o usuário disser que sim, ou quando ele aprovar três mensagens seguidas sem pedir mudança. Se voltar a corrigir bastante, volte para `em ajuste`.

Peça confirmação antes de gravar qualquer mudança que contradiga uma regra existente.
