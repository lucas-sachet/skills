---
name: mapa-do-projeto
description: Planeja um projeto grande demais para uma conversa só, como um mapa de decisões em arquivos, e resolve uma decisão por vez até o caminho ficar claro.
disable-model-invocation: true
---

Chegou uma ideia solta, grande demais para uma conversa só e envolta em névoa: o caminho daqui até o **destino** ainda não está visível. Esta skill existe para achar esse caminho, e não para correr até o destino. Ela desenha o caminho como um **mapa** em arquivos, e depois trabalha as **decisões** (perguntas cuja resposta é uma escolha, e não etapas de execução) uma por vez, até a rota ficar clara.

O destino varia a cada projeto, e nomeá-lo é o primeiro ato: ele molda todas as decisões. Pode ser um plano pronto para executar, uma escolha a travar antes de começar, ou uma mudança a fazer (trocar de sistema, abrir uma filial, lançar um produto).

## Planejar, não executar

Por padrão, o mapa é de **planejamento**: cada decisão resolve uma escolha, e o mapa termina quando o caminho está claro e nada falta decidir antes de alguém ir fazer. A vontade de simplesmente fazer o trabalho costuma ser o sinal de que você chegou à borda do mapa e é hora de passar adiante (use `/montar-plano`). Um projeto pode mudar isso em suas **Notas**, mas, sem isso, produza decisões, não entregas.

## Chame pelo nome

Todo mapa e toda decisão tem um **nome**: o título. Em tudo o que o usuário lê, refira-se a cada um pelo nome, nunca só pelo número. Uma lista de "decisão 4, 7, 9" é ilegível; nomes se leem de relance.

## O mapa

O mapa vive numa pasta `mapa-<assunto>/`, com um arquivo `MAPA.md` (o mapa em si) e uma pasta `decisoes/` (uma decisão por arquivo, `NN-titulo.md`).

O mapa é um **índice**, não um depósito. Ele lista as decisões tomadas e aponta para os arquivos que guardam os detalhes. Uma decisão vive em um único lugar, o arquivo dela; o mapa só resume em uma linha e faz o link.

### O corpo do `MAPA.md`

O projeto inteiro em baixa resolução, lido uma vez por sessão. As decisões abertas não são listadas aqui: são os arquivos de `decisoes/` ainda não resolvidos.

```markdown
# Mapa: <nome do projeto>

## Destino

<como é chegar ao fim deste mapa: o plano, a escolha ou a mudança que se busca. Uma ou duas linhas; toda sessão se orienta por isto antes de escolher uma decisão.>

## Notas

<o assunto; skills que toda sessão deve consultar; preferências fixas deste projeto>

## Decisões até agora

- [<título da decisão resolvida>](decisoes/NN-titulo.md): <resumo da resposta em uma linha>

## Ainda não especificado

<névoa dentro do escopo que ainda não dá para transformar em decisão; vira decisão conforme o caminho avança>

## Fora do escopo

<o que foi descartado deste projeto; nunca volta, a não ser que o destino seja redesenhado>
```

### Decisões

Cada decisão é um arquivo em `decisoes/`, com o número e o título no nome. O corpo é a pergunta, com tamanho para caber em uma conversa:

```markdown
# <NN>: <Título>

**Tipo:** pesquisar | rascunho | questionar | tarefa

**Depende de:** <decisões que travam esta, ou "Nenhuma">

**Situação:** aberta | resolvida

## Pergunta

<a escolha ou investigação que esta decisão resolve>
```

A resposta não fica no corpo inicial: é registrada ao resolver (veja [Percorrer o mapa](#percorrer-o-mapa)). Materiais criados na decisão (rascunhos, pesquisas) ficam em arquivos ao lado e são apontados, não colados.

Uma decisão está **liberada** quando todas as que a travam estão resolvidas. A **fronteira** é o conjunto das decisões abertas e liberadas: a borda do que se conhece.

## Tipos de decisão

Cada decisão é **com humano** (feita junto com o usuário, que fala por si) ou **sozinha** (o Claude resolve por conta própria). Uma decisão com humano só se resolve nessa conversa ao vivo; o Claude nunca responde no lugar do usuário (um "questionar" que responde às próprias perguntas quebrou a regra).

- **Pesquisar** (sozinha): ler documentos, sites oficiais ou materiais para achar um fato de que uma decisão depende. Resolvida por um subagente que chama a skill `pesquisar`. Use quando for preciso saber algo de fora.
- **Rascunho** (com humano): subir o nível da conversa fazendo algo barato, simples e concreto para reagir (um esboço de página, um texto-modelo, uma tabela de preços de teste). Aponte o rascunho na decisão. Use quando a pergunta central for "como deve ser" ou "como deve funcionar".
- **Questionar** (com humano): conversa. É o caso padrão. Chame sempre a skill `questionar`.
- **Tarefa** (com humano ou sozinha): trabalho manual que precisa acontecer antes de se poder _decidir_: criar uma conta para avaliar uma ferramenta, liberar um acesso, juntar dados para ver o formato. É o único tipo que _faz_ em vez de decidir, e só existe para destravar uma decisão. Resolvida quando o trabalho está feito; a resposta registra o que foi feito e fatos de que decisões seguintes dependem.

## Névoa

O mapa é _deliberadamente_ incompleto: não desenhe o que ainda não enxerga. Além das decisões ativas há a **névoa**: a visão turva das escolhas que você sabe que virão, mas ainda não consegue formular, porque dependem de perguntas em aberto. Resolver uma decisão limpa a névoa à frente e transforma o que já dá para especificar em decisões novas, uma por vez, até o caminho estar claro e não restar nenhuma.

A seção **Ainda não especificado** é onde essa visão turva é anotada: a pergunta suspeita, a área para voltar depois. É a fronteira ainda desconhecida _em direção_ ao destino: tudo ali está no escopo, só não está nítido o bastante para virar decisão.

**Névoa ou decisão?** O teste é se você consegue formular a pergunta com precisão agora, e _não_ se consegue respondê-la agora.

- **Decisão** quando a pergunta já está nítida, mesmo que esteja travada.
- **Ainda não especificado** quando você ainda não consegue formulá-la com nitidez. Não fatie a névoa em pedaços do tamanho de uma decisão: ela é mais grossa. Um trecho pode virar várias decisões, ou nenhuma, quando a fronteira chegar nele.

**Ainda não especificado** exclui o que já foi decidido, o que já é uma decisão aberta e o que está fora do escopo.

## Fora do escopo

A névoa só se forma _em direção_ ao destino. O destino define o escopo, então o que fica além dele está **fora do escopo**: não é névoa e não pertence a **Ainda não especificado**. Vai para a seção **Fora do escopo**: o que você decidiu conscientemente deixar de fora _deste_ projeto.

O que está fora do escopo nunca volta, a não ser que o destino seja redesenhado, e então como um projeto novo.

Descartar algo é um ato de escopo, não um passo no caminho. Quando uma decisão que já existe se revela além do destino, **marque-a como descartada** e deixe uma linha em **Fora do escopo**: o resumo e o motivo, com o link. Ela não entra em **Decisões até agora**, que registra a rota realmente percorrida.

## Como usar

Dois modos. Em ambos, **nunca resolva mais de uma decisão por sessão**, exceto as de pesquisar.

### Desenhar o mapa

O usuário chega com uma ideia solta.

1. **Nomeie o destino.** Chame a skill `questionar` para fixar aonde este mapa quer chegar: o plano, a escolha ou a mudança. O destino define o escopo, então vem primeiro.
2. **Mapeie a fronteira.** Questione de novo, agora **em largura**: abra o leque pelo espaço inteiro em vez de ir fundo em um fio só, trazendo as decisões em aberto e os primeiros passos possíveis agora. **Se não aparecer névoa** (o caminho já está claro e a jornada é pequena o bastante para uma conversa), não precisa de mapa. Pare e pergunte ao usuário como prefere seguir.
3. **Crie a pasta e o `MAPA.md`**: Destino e Notas preenchidos, Decisões até agora vazio, a névoa esboçada em **Ainda não especificado**.
4. **Crie as decisões que já dá para especificar**, um arquivo cada, e ligue as dependências numa **segunda passada** (os arquivos precisam existir antes de se referenciarem). Isso separa a fronteira das decisões travadas; o que ainda não dá para especificar fica na névoa.
5. **Dispare as pesquisas.** Para cada decisão do tipo `pesquisar` criada, chame um subagente que use a skill `pesquisar` para resolvê-la em paralelo, guardando o resultado em arquivo ao lado da decisão.
6. Pare: desenhar é o trabalho de uma sessão; não resolva nenhuma decisão à mão.

### Percorrer o mapa

O usuário chega com um mapa (a pasta). Uma decisão é **opcional**: sem ela, quem escolhe a próxima é você, não o usuário.

1. Carregue o **mapa**: a visão de baixa resolução, e não o corpo de todas as decisões.
2. Escolha a decisão. Se o usuário indicou uma, use-a. Senão, pegue a primeira da fronteira, na ordem.
3. Resolva-a conforme o **tipo** (veja [Tipos de decisão](#tipos-de-decisão)). Leia o tipo no arquivo, e não só o corpo. **Aproxime quando precisar**: abra o corpo completo de qualquer decisão relacionada ou resolvida; chame as skills que o bloco `## Notas` indicar. Na dúvida, chame a skill `questionar`.
4. Registre a resolução: escreva a resposta no arquivo da decisão, mude a situação para **resolvida** e acrescente uma linha em **Decisões até agora** no mapa, com o link.
5. Acrescente as decisões que surgiram; transforme em decisão a névoa que a resposta tornou especificável, tirando cada trecho de **Ainda não especificado** para ele viver só como decisão. Se a resposta revelar que uma decisão (esta ou outra) fica além do destino, **marque como fora do escopo** em vez de resolvê-la na rota. Se a decisão invalidar outras partes do mapa, atualize ou apague essas decisões.
