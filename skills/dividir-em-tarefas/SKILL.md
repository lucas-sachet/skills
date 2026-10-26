---
name: dividir-em-tarefas
description: Divide um plano (ou a conversa atual) em tarefas pequenas e ordenadas, cada uma dizendo do que depende e como saber que está pronta, num arquivo de checklist.
disable-model-invocation: true
---

# Dividir em tarefas

Divida um plano, ou o que foi combinado na conversa, em **tarefas**: fatias pequenas e completas, cada uma dizendo de quais outras **depende**.

## Processo

### 1. Reúna o contexto

Trabalhe com o que já está na conversa. Se o usuário passar um arquivo (por exemplo o `plano-<assunto>.md` de `/montar-plano`), leia-o inteiro.

### 2. Rascunhe fatias completas

Divida o trabalho em **fatias completas**.

<regras-da-fatia>

- Cada fatia atravessa o caminho inteiro, do começo ao fim, em vez de fazer só uma parte de tudo. Exemplo: "fazer um pedido de teste de ponta a ponta, do orçamento à entrega" vale mais do que "montar todos os modelos de orçamento" e depois "montar todos os modelos de entrega".
- Uma fatia pronta pode ser vista, testada ou usada sozinha.
- Cada fatia cabe numa conversa só com o Claude, ou num dia de trabalho de uma pessoa.
- Preparativos (arrumar, juntar documentos, liberar acessos) vêm primeiro.

</regras-da-fatia>

Diga de quais outras tarefas cada uma **depende**: as que precisam terminar antes de ela começar. Uma tarefa sem dependências pode começar já.

**Trocas de sistema ou de processo são a exceção.** Quando a mudança afeta tudo de uma vez (trocar a planilha pelo sistema novo, mudar o fornecedor de todos os produtos), não force em fatias. Faça em três tempos: primeiro **monte o novo ao lado do antigo**, para nada parar; depois **migre aos poucos** (por setor, por cliente, por loja), uma tarefa para cada lote; por fim **desligue o antigo**, numa tarefa que depende de todos os lotes.

Indique também **quem faz** cada tarefa: o Claude, o usuário, ou outra pessoa.

### 3. Valide com o usuário

Apresente a divisão como lista numerada. Para cada tarefa, mostre:

- **Título**: nome curto e descritivo
- **Depende de**: quais tarefas precisam terminar antes (se houver)
- **Quem faz**: Claude, você ou outra pessoa
- **O que entrega**: o resultado completo que esta tarefa faz funcionar

Pergunte ao usuário:

- O tamanho das tarefas está certo? (grandes demais / pequenas demais)
- As dependências estão corretas: cada tarefa depende só do que realmente a trava?
- Alguma tarefa deve ser juntada ou dividida?

Itere até o usuário aprovar.

### 4. Salve a lista

Salve as tarefas aprovadas num único arquivo `tarefas-<assunto>.md` na pasta atual, numeradas a partir de `01` na ordem de dependência (as que destravam outras primeiro), usando o modelo abaixo.

Trabalhe pela **fronteira**: qualquer tarefa cujas dependências estejam todas concluídas. Numa cadeia simples, é de cima para baixo.

NÃO altere nem apague o plano de origem.

<modelo-de-tarefas>

# Tarefas: <nome do projeto>

## 01: <Título da tarefa>

**O que entrega:** o resultado completo que esta tarefa faz funcionar, do ponto de vista de quem usa, e não uma lista de passos internos.

**Depende de:** os números e títulos das tarefas que travam esta, ou "Nenhuma (pode começar já)".

**Quem faz:** Claude, você ou <pessoa>

**Situação:** pronta para começar

- [ ] Critério de pronto 1
- [ ] Critério de pronto 2

## 02: <Título da tarefa>

...

</modelo-de-tarefas>

Evite detalhes que mudam rápido, como nomes de arquivos, preços do dia ou links. Exceção: se um rascunho produziu um trecho que registra uma decisão com mais precisão do que a prosa (uma fórmula de cálculo, uma tabela de preços, um texto de contrato), inclua-o na tarefa e anote que veio de um rascunho. Corte para o que importa na decisão, não para uma versão completa.
