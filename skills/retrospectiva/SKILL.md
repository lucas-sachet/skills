---
name: retrospectiva
description: Faz uma retrospectiva de uma conversa de trabalho com o Claude e sugere melhorias para as próximas ficarem mais rápidas e certeiras. Use quando o usuário quiser revisar o que funcionou e o que não funcionou numa sessão.
disable-model-invocation: true
---

O usuário pediu uma **retrospectiva**. Você vai sugerir melhorias no **ambiente de trabalho do Claude** (instruções, arquivos, acesso a informações e skills) para que as próximas conversas rendam mais.

## Passos

1. Chame a ferramenta de skills com `primeiros-passos` para ler o guia de como escrever instruções para o Claude.

2. Leia as fontes primárias da sessão que o usuário indicar. Pode ser preciso procurar nos históricos de conversa deste computador. Se o usuário não indicar, use a conversa atual.

3. Procure oportunidades de melhoria nestas categorias:

- **Contexto que faltou**: o Claude precisou perguntar ou errou por não conhecer o negócio (produtos, preços, clientes, tom de voz, regras da empresa)? _Use quando_ o usuário teve que explicar a mesma coisa mais de uma vez. A solução costuma ser anotar essa informação num arquivo de instruções (`CLAUDE.md`) para o Claude ler sempre.
- **Encontrar as coisas**: foi fácil para o Claude achar os arquivos certos (planilhas, contratos, modelos de e-mail)? Os documentos estão espalhados, com nomes confusos ou duplicados? _Use quando_ a sessão demorou para achar uma informação. Um arquivo-índice curto, apontando onde cada coisa fica, resolve muito.
- **Conferências**: houve erros que uma checagem simples teria pego (conferir números, datas, nomes de clientes, um checklist antes de enviar)? _Use quando_ o Claude errou algo que uma regra fixa evitaria.
- **Instruções demais ou de menos**: o arquivo de instruções está grande e cheio de regras que não mudam nada no comportamento? Há regras que deveriam virar um checklist ou uma skill? _Use quando_ o arquivo de instruções estiver longo e difícil de manter, no projeto ou no escopo global do usuário.
- **Passos caros**: o Claude gastou muito tempo ou volume de leitura em algo que poderia ser mais direto (ler um arquivo enorme inteiro, pesquisar o mesmo assunto de novo)? _Use quando_ a sessão foi lenta ou longa sem necessidade.
- **Acesso a informação**: faltou alguma informação importante que o Claude não conseguia alcançar (um sistema, uma planilha, um site que exige login)? _Use quando_ um dado essencial não estava disponível.
- **Uso das skills**: existia uma skill que resolveria a tarefa e não foi usada, ou uma tarefa repetida que merece virar skill? _Use quando_ o usuário repetiu um tipo de pedido várias vezes.

4. Apresente as sugestões ao usuário, da mais importante para a menos, em linguagem simples. Para cada uma, diga o que aconteceu na sessão, o que mudar e onde (qual arquivo ou skill).

## Referência

### Arquivos úteis

- `CLAUDE.md`: lido pelo Claude no início de toda conversa naquela pasta. Use com muita economia, quase só para **ponteiros** que dizem onde achar as coisas e para regras que o Claude não adivinharia.
- Documentos de apoio (tabela de preços, tom de voz, perguntas frequentes de clientes): guarde em arquivos próprios, apontados pelo `CLAUDE.md`. Procure um que já exista antes de criar outro.
- Skills: use para tarefas que se repetem ou para conhecimento que só deve entrar na conversa quando necessário. Siga o conselho da skill `primeiros-passos`.
