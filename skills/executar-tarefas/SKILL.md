---
name: executar-tarefas
description: Executa o trabalho de um plano ou de uma lista de tarefas, uma a uma, conferindo o resultado contra o critério de pronto.
disable-model-invocation: true
---

Execute o trabalho descrito pelo usuário no plano ou na lista de tarefas.

Se o usuário indicar uma tarefa (por exemplo "tarefa 03" do `tarefas-<assunto>.md`), leia-a e diga o título antes de começar. Se a referência for ambígua, pergunte. Se ele não indicar, comece pela primeira tarefa da fronteira (a primeira cujas dependências já estejam concluídas).

Faça só as tarefas cujo responsável seja o Claude. Para as que são do usuário ou de outra pessoa, diga o que precisa ser feito e espere a confirmação antes de seguir.

Para cada tarefa:

1. Faça o trabalho e salve o resultado onde o usuário vai achar, dizendo o caminho.
2. Confira o resultado contra cada **critério de pronto** da tarefa, um por um, e diga o que foi verificado e como.
3. Marque a tarefa como concluída no arquivo de tarefas e mostre ao usuário o que foi entregue.
4. Pare e peça aprovação antes de passar para a próxima, a menos que o usuário tenha pedido para seguir direto.

Se algo não puder ser verificado (um dado que só o usuário tem, uma decisão que ficou em aberto), diga claramente o que ficou sem conferir em vez de dar a tarefa como pronta.

Ao terminar, chame a ferramenta de skills com `retrospectiva` se o usuário quiser revisar o que funcionou e o que não funcionou.
