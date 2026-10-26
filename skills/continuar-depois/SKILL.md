---
name: continuar-depois
description: Resume a conversa atual num documento para você (ou outro agente) continuar o trabalho numa conversa nova, sem perder o contexto.
argument-hint: "Para que a próxima conversa vai servir?"
disable-model-invocation: true
---

Escreva um documento de continuidade que resuma a conversa atual, para que uma conversa nova possa seguir o trabalho sem começar do zero. Salve na pasta temporária do sistema do usuário (`$TMPDIR`, senão `/tmp`; `%TEMP%` no Windows), e não na pasta de trabalho atual.

Inclua uma seção de "skills sugeridas", dizendo quais skills a próxima conversa deve usar.

Não repita o que já está registrado em outros lugares (planos, documentos, e-mails, commits). Aponte para eles pelo caminho ou link.

Remova qualquer informação sensível, como senhas, chaves de acesso e dados pessoais de clientes ou funcionários.

Se o usuário passou um argumento, trate-o como a descrição do foco da próxima conversa e ajuste o documento a ele.

Ao terminar, diga ao usuário em linguagem simples onde o arquivo foi salvo e o que colar na conversa nova, por exemplo: "Leia o arquivo <caminho> e continue de onde paramos."
