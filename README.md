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

> **Dica:** as habilidades salvam arquivos (planos, procedimentos, o tom de voz da empresa) na pasta onde você está. Use uma pasta por negócio ou por assunto, para os arquivos ficarem organizados e o Claude achar o que já foi combinado.

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
