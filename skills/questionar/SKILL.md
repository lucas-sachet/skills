---
name: questionar
description: Questiona o usuário a fundo sobre um plano, decisão ou ideia até os dois terem o mesmo entendimento. Use quando o usuário quiser testar o próprio raciocínio, disser "me questiona", "me pressiona", "testa meu plano", "estou em dúvida se", ou usar qualquer expressão parecida com "dúvida".
---

Entreviste o usuário sem pressa e sem dó, até vocês chegarem a um entendimento compartilhado. Pense no assunto como uma **árvore de decisões**: cada decisão abre outras decisões que dependem dela. Por exemplo, "vou abrir uma segunda loja" abre "onde", "com que dinheiro" e "quem vai gerenciar", e cada uma dessas abre mais perguntas.

Percorra a árvore em **rodadas**. A **fronteira** é o conjunto de decisões cujas pré-condições já estão resolvidas: as perguntas que você pode fazer _agora_ sem chutar respostas que ainda não ouviu. Faça toda a fronteira numa rodada só: numere as perguntas e dê a sua resposta recomendada para cada uma. Depois espere o usuário responder antes da próxima rodada.

Formate cada rodada assim utilizando ferramenta _askQuestion_:

```
**P1** - **<título da pergunta>**: <texto da pergunta, pode ter vários parágrafos, inclusive alternativas>

➡️ <sua resposta recomendada>

---

**P2** - **<título da pergunta>**: <texto da pergunta, pode ter vários parágrafos, inclusive alternativas>

➡️ <sua resposta recomendada>
```

Escreva cada pergunta de modo que responder "sim" signifique aceitar a sua recomendação.

Cada rodada respondida muda a árvore: decisões resolvidas empurram a fronteira para a frente e liberam perguntas que dependiam delas. Recalcule a fronteira e faça a próxima rodada. Uma pergunta cuja resposta depende de outra pergunta ainda em aberto nesta rodada fica para uma rodada _posterior_.

Descobrir _fatos_ é trabalho seu, nunca do usuário. Se uma pergunta precisa de um fato que está nos arquivos ou nas ferramentas à sua disposição (uma planilha, um documento, um site), vá buscar você mesmo, ou peça a um subagente que busque. Não pergunte nada que você consiga descobrir sozinho. Não fique parado esperando: uma busca em andamento é uma pré-condição ainda aberta, então só as perguntas que dependem dela esperam o resultado. Faça o resto da fronteira agora. As _decisões_ são do usuário: apresente cada uma e espere.

Use linguagem simples. Se precisar de um termo técnico, explique em uma frase. Prefira exemplos do dia a dia do negócio (clientes, preços, equipe, prazos, caixa) e perguntas que o usuário consiga responder sem consultar ninguém.

A sessão termina quando a fronteira está vazia: todos os ramos da árvore foram visitados e nada ficou assumido em silêncio. Não execute nada do que foi combinado até o usuário confirmar que vocês chegaram a um entendimento compartilhado.
