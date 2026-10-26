# Habilidades

Um conjunto de **habilidades (skills) para o Claude**, em português do Brasil, feitas para donos de negócio e para as pessoas que trabalham com eles. Você não precisa saber programar nem entender como a IA funciona por dentro.

## O que é uma habilidade?

É um conjunto de instruções que ensina o Claude a fazer uma tarefa do jeito certo, toda vez. Em vez de explicar do zero o que você quer ("escreve um e-mail para um cliente, mas educado, e não promete nada, e..."), você digita um comando curto, como `/responder-cliente`, e o Claude já sabe o roteiro: faz as perguntas certas, evita os erros comuns e guarda o resultado num arquivo.

## Para quem é

Para quem toca um negócio e quer usar o Claude no dia a dia sem virar especialista: planejar a semana, responder clientes, documentar processos, revisar preços, tomar decisões e escrever textos.

Se você está começando e não sabe por onde ir, digite `/primeiros-passos`. O Claude pergunta o que você quer resolver e aponta a habilidade certa.

## Instalação

Você precisa ter o **Claude Code** instalado. Depois, no terminal:

```bash
claude plugin marketplace add lucas-sachet/skills
claude plugin install habilidades@lucas-sachet
```

Para usar, abra o Claude Code numa pasta do seu negócio e digite `/` seguido do nome da habilidade (por exemplo, `/questionar`). O Claude Code mostra a lista enquanto você digita.

### Se o terminal diz que o `claude` não é reconhecido

Isso acontece quando o Claude Code está instalado, mas o computador não sabe onde ele fica (o PATH). Você não precisa consertar isso sozinho: copie o texto abaixo, cole numa conversa com o Claude (por exemplo, na extensão do Claude Code no VS Code) e envie. Ele faz a instalação por você.

```text
Quero instalar o plugin "Habilidades" no Claude Code, e quero que você faça tudo por mim, sem me pedir para rodar nenhum comando.

1. Descubra se o comando `claude` funciona no terminal.
2. Se não funcionar, procure o programa (`claude.exe`, por exemplo em `%USERPROFILE%\.local\bin` ou dentro da pasta da extensão do Claude Code no VS Code) e use o caminho completo dele.
3. Rode `claude plugin marketplace add lucas-sachet/skills` e depois `claude plugin install habilidades@lucas-sachet`.
4. Confirme que deu certo com `claude plugin list`.
5. No final, explique em linguagem simples o que você fez e o que eu preciso fazer para começar a usar (por exemplo, abrir uma conversa nova e digitar /primeiros-passos).

Não mude nenhuma outra configuração do meu computador. Se for preciso alterar o PATH, me pergunte antes e explique por quê.
```

> **Dica:** as habilidades salvam arquivos (planos, procedimentos, o tom de voz da empresa) na pasta onde você está. Use uma pasta por negócio ou por assunto, para os arquivos ficarem organizados e o Claude achar o que já foi combinado.

## Como remover

Você pode tirar as habilidades a qualquer momento. Seus arquivos (planos, procedimentos, tom de voz) ficam nas suas pastas e **não são apagados**.

Para desinstalar:

```bash
claude plugin uninstall habilidades
claude plugin marketplace remove lucas-sachet
```

O primeiro comando remove o plugin. O segundo tira a fonte de onde ele veio, e só é necessário se você não pretende reinstalar. Abra uma conversa nova para a mudança valer.

Se prefere só pausar, sem desinstalar, use `claude plugin disable habilidades` (e `claude plugin enable habilidades` para voltar).

Se o terminal não reconhece o `claude`, peça ao próprio Claude: *"Desinstale o plugin Habilidades do Claude Code (`claude plugin uninstall habilidades` e depois `claude plugin marketplace remove lucas-sachet`), usando o caminho completo do `claude.exe` se for preciso, e me diga quando terminar."*

## As habilidades

### Para começar

| Habilidade | Para que serve |
| --- | --- |
| [primeiros-passos](skills/primeiros-passos/SKILL.md) | Descobrir por onde começar, qual habilidade usar e como pedir melhor |
| [explicar-de-novo](skills/explicar-de-novo/SKILL.md) | "Não entendi": o Claude explica de novo, mais simples |
| [ensinar](skills/ensinar/SKILL.md) | Aprender um assunto novo aos poucos, com aulas guiadas |

### Planejar e decidir

| Habilidade | Para que serve |
| --- | --- |
| [planejar-semana](skills/planejar-semana/SKILL.md) | Escolher as prioridades da semana, distribuir nos dias e revisar na sexta |
| [questionar](skills/questionar/SKILL.md) | Testar um plano ou decisão com perguntas duras, uma rodada por vez |
| [montar-plano](skills/montar-plano/SKILL.md) | Transformar uma conversa num plano escrito |
| [dividir-em-tarefas](skills/dividir-em-tarefas/SKILL.md) | Dividir um plano em tarefas pequenas e ordenadas |
| [executar-tarefas](skills/executar-tarefas/SKILL.md) | Fazer as tarefas de um plano, uma a uma, conferindo o resultado |
| [mapa-do-projeto](skills/mapa-do-projeto/SKILL.md) | Planejar um projeto grande, decisão por decisão |
| [braco-direito](skills/braco-direito/SKILL.md) | Perseguir uma meta longa, coordenando agentes e guardando a memória |

### Documentos e processos

| Habilidade | Para que serve |
| --- | --- |
| [escrever-procedimento](skills/escrever-procedimento/SKILL.md) | Documentar um processo (SOP/POP) para qualquer pessoa conseguir seguir |
| [fazer-questionario](skills/fazer-questionario/SKILL.md) | Transformar uma dúvida em perguntas para outra pessoa responder (contador, fornecedor, sócio) |
| [pesquisar](skills/pesquisar/SKILL.md) | Pesquisar um assunto em fontes confiáveis e guardar o resultado |

### Clientes, marketing e vendas

| Habilidade | Para que serve |
| --- | --- |
| [responder-cliente](skills/responder-cliente/SKILL.md) | Escrever e-mails e mensagens no tom de voz da sua empresa, que melhora a cada uso |
| [revisar-oferta](skills/revisar-oferta/SKILL.md) | Revisar preço e oferta, com contas de margem e testes pequenos |

### Escrever textos

Um fluxo em três etapas, para artigos, posts e discursos:

| Etapa | Habilidade | Para que serve |
| --- | --- | --- |
| 1 | [escrever-ideias](skills/escrever-ideias/SKILL.md) | Juntar ideias soltas, sem estrutura ainda |
| 2 | [escrever-roteiro](skills/escrever-roteiro/SKILL.md) | Montar o texto momento a momento, escolhendo o caminho |
| 3 | [escrever-rascunho](skills/escrever-rascunho/SKILL.md) | Transformar o material num texto, parágrafo a parágrafo |

### Melhorar o uso do Claude

| Habilidade | Para que serve |
| --- | --- |
| [continuar-depois](skills/continuar-depois/SKILL.md) | Resumir a conversa para continuar em outra, sem perder o contexto |
| [retrospectiva](skills/retrospectiva/SKILL.md) | Revisar uma conversa e melhorar as próximas |

## Cuidados ao usar

- **Confira o que importa.** O Claude pode errar números, datas, leis e preços. Revise antes de enviar ou decidir.
- **Proteja dados sensíveis.** Não cole senhas, dados de cartão ou dados pessoais de clientes sem necessidade.
- **Assuntos jurídicos, contábeis e tributários** pedem um profissional. As habilidades avisam quando isso se aplica.

## Estado do projeto

Em construção. As habilidades foram escritas e revisadas, mas ainda estão sendo testadas no uso real.

## Créditos e licença

Baseado em [mattpocock/skills](https://github.com/mattpocock/skills), de Matt Pocock, e adaptado para o público de negócios por Lucas Sachet. Licença MIT (veja [LICENSE](LICENSE)).
