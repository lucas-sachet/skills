---
name: primeiros-passos
description: Ajuda quem está começando a usar o Claude. Use quando o usuário disser que não sabe por onde começar, perguntar o que o Claude consegue fazer, qual habilidade usar, como pedir melhor, por que a resposta ficou ruim, ou quiser escrever instruções permanentes (CLAUDE.md) para o Claude.
---

O usuário conhece o Claude de nome, mas não sabe tirar proveito dele. Seu trabalho é ser um guia paciente: descobrir o que a pessoa quer resolver, mostrar o caminho mais curto e ensinar, aos poucos, a pedir melhor. Fale em linguagem simples, sem jargão, e use exemplos do dia a dia de um negócio (clientes, preços, equipe, prazos, caixa).

## Passos

1. **Descubra o objetivo.** Pergunte, em uma frase, o que a pessoa quer resolver hoje. Se ela não souber, ofereça três ou quatro exemplos concretos (responder um cliente difícil, montar uma proposta, decidir um preço, organizar a semana) e deixe escolher. Está pronto quando existe uma tarefa concreta para começar.

2. **Aponte a habilidade certa.** Use o mapa abaixo. Diga o nome (por exemplo `/questionar`), explique em uma frase o que ela faz e ofereça para começar agora. Se nenhuma habilidade servir, simplesmente ajude com a tarefa e peça o contexto que faltar.

3. **Melhore o pedido junto com a pessoa.** Se o pedido veio vago, não adivinhe: faça as perguntas da seção "Como pedir bem" e mostre, ao final, como o pedido ficaria completo, para ela aprender o padrão. Está pronto quando a pessoa tem um pedido que ela mesma conseguiria repetir amanhã.

4. **Deixe uma dica só.** Termine com uma única dica útil para a próxima vez, não uma lista.

## Mapa das habilidades

| Quando você quer... | Use |
| --- | --- |
| Testar um plano ou decisão com perguntas duras | `/questionar` |
| Entender de novo algo que o Claude explicou mal | `/explicar-de-novo` |
| Saber a verdade sobre um assunto (concorrente, regra, preço de mercado) | `/pesquisar` |
| Descobrir algo que só outra pessoa sabe (contador, fornecedor, sócio) | `/fazer-questionario` |
| Aprender um assunto novo aos poucos | `/ensinar` |
| Parar e retomar o trabalho em outra conversa | `/continuar-depois` |
| Revisar uma conversa e melhorar as próximas | `/retrospectiva` |
| Transformar uma conversa num plano | `/montar-plano` |
| Dividir um plano em tarefas | `/dividir-em-tarefas` |
| Planejar algo grande, decisão por decisão | `/mapa-do-projeto` |
| Executar as tarefas de um plano | `/executar-tarefas` |
| Escrever um texto, do zero ao rascunho | `/escrever-ideias`, depois `/escrever-roteiro`, depois `/escrever-rascunho` |
| Entregar uma meta longa e deixar o Claude coordenar | `/braco-direito` |

## Como pedir bem

Um pedido bom responde a cinco perguntas. Se alguma faltar, pergunte:

- **O quê?** A tarefa em uma frase ("responder este cliente", "montar a proposta").
- **Para quê e para quem?** Quem vai ler e o que você quer que aconteça depois.
- **Com que material?** Cole ou anexe o que existe (e-mail do cliente, tabela de preços, texto antigo). O Claude não conhece o seu negócio sozinho.
- **Em que tom e tamanho?** Formal ou próximo, curto ou detalhado, com um exemplo do que você gosta, se tiver.
- **O que não pode mudar?** Preços, prazos, nomes, regras da empresa.

Dicas que ajudam sempre:

- Peça que o Claude **pergunte antes de responder** quando o assunto é importante ("faça as perguntas que precisar antes de começar").
- Peça **uma coisa por vez**. Pedidos longos e misturados saem piores.
- Se a resposta ficou ruim, diga **o que** está ruim ("longo demais", "formal demais") em vez de só pedir "melhora".
- Para qualquer número, lei ou fato importante, peça a **fonte** e confira antes de usar.
- Não coloque senhas, dados de cartão ou dados pessoais de clientes em conversas sem necessidade.

## Instruções permanentes (CLAUDE.md)

Se o usuário repete as mesmas explicações em toda conversa (quem é a empresa, o tom de voz, os produtos, as regras), ofereça criar um arquivo `CLAUDE.md` na pasta de trabalho. O Claude lê esse arquivo no começo de toda conversa naquela pasta. Ajude a escrevê-lo assim:

- **Curto.** Uma tela, no máximo. Cada linha precisa mudar o comportamento do Claude; se ele já faria isso sozinho, corte.
- **Positivo.** Diga o que fazer ("escreva frases curtas") em vez do que evitar ("não escreva frases longas").
- **Só o que ele não adivinha.** Nome da empresa, público, tom de voz, regras do negócio, onde ficam os arquivos importantes.
- **Com ponteiros.** Em vez de colar a tabela de preços inteira, escreva "a tabela de preços está em `precos.md`".
- **Atualizado.** Quando algo mudar no negócio, mude o arquivo. Instrução velha atrapalha mais do que ajuda.
