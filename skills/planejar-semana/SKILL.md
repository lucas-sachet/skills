---
name: planejar-semana
description: Monta o plano da semana de quem toca um negócio: escolhe as poucas prioridades que importam, distribui nos dias e separa o que delegar ou adiar. Use quando o usuário disser "planejar minha semana", "organizar a semana", "o que priorizar", "estou sobrecarregado" ou no começo/fim de semana.
---

Ajude o usuário a sair da segunda-feira com um plano que cabe na semana real dele, não na semana ideal. O erro mais comum é uma lista grande demais: seu trabalho é cortar, não só organizar.

## Passos

1. **Retome a semana anterior.** Procure na pasta atual o arquivo `semana-AAAA-MM-DD.md` mais recente. Se existir, leia o que ficou pendente e o que foi combinado como "como saberei na sexta". Se não existir, siga adiante sem comentar.

2. **Pergunte tudo de uma vez, em uma só mensagem curta.** Não faça uma pergunta por vez. Peça:
   - O que ficou pendente ou travado da semana passada?
   - Que compromissos fixos já existem (reuniões, entregas, visitas, prazos)?
   - Se a semana der certo, quais 1 a 3 resultados fariam você dizer "valeu a pena"?
   - Quanto tempo livre você realmente tem por dia, e quem pode ajudar?
   - Há algo que você tem adiado e que está pesando?

   Se o usuário não souber responder tudo, trabalhe com o que ele disser e anote as suposições. Está pronto quando você consegue listar os compromissos fixos e pelo menos um resultado desejado.

3. **Escolha as prioridades.** Separe cada item em uma destas quatro gavetas:
   - **Fazer esta semana** (no máximo 3 itens de peso, mais tarefas pequenas): o que move o negócio ou evita um problema real.
   - **Delegar**: o que outra pessoa (ou o Claude) pode fazer, e a quem.
   - **Adiar**: o que pode esperar, com uma data para voltar a olhar.
   - **Largar**: o que não vale mais o esforço. Diga isso com todas as letras quando for o caso.

   Se a lista de "fazer esta semana" passar da capacidade de tempo informada, não encaixe tudo: devolva ao usuário uma escolha clara ("cabe A ou B, qual pesa mais?") com a sua recomendação.

4. **Distribua nos dias.** Ponha os itens de peso nos horários de maior energia do usuário, deixe cerca de 20% do tempo livre para imprevistos, e encaixe as tarefas pequenas nos intervalos. Não agende dois itens de peso para o mesmo bloco.

5. **Salve o plano.** Grave em `semana-AAAA-MM-DD.md` (data da segunda-feira) na pasta atual, com o modelo abaixo, e mostre o resumo ao usuário. Está pronto quando o usuário sabe qual é a primeira coisa que faz amanhã.

6. **Ofereça a revisão de sexta.** Diga que, na sexta, basta pedir "revisar a semana" para comparar o que aconteceu com este plano e preparar a próxima.

<modelo-da-semana>

# Semana de <data da segunda-feira>

## Resultados que fariam a semana valer

1. ...

## Compromissos fixos

- Seg 10h: ...

## Plano por dia

**Segunda:** ...
**Terça:** ...
**Quarta:** ...
**Quinta:** ...
**Sexta:** ...

## Delegar

- <tarefa>: <quem>, até <quando>

## Adiar

- <item>: voltar a olhar em <data>

## Largar

- <item>: <motivo>

## Riscos da semana

O que pode atrapalhar e o que fazer se acontecer.

## Como saberei na sexta

Sinais concretos de que a semana deu certo.

</modelo-da-semana>

## Revisar a semana

Quando o usuário pedir para revisar, leia o `semana-*.md` mais recente e pergunte, em uma mensagem só: o que foi feito, o que não foi e por quê, e o que surpreendeu. Compare com "Como saberei na sexta". Diga uma coisa que funcionou e uma a mudar na próxima semana, e leve o que ficou pendente para o plano seguinte.
