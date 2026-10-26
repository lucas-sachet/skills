---
name: ensinar
description: Ensina ao usuário uma habilidade ou conceito novo (por exemplo ler um fluxo de caixa, precificar, vender melhor, usar uma ferramenta), em várias sessões, dentro de uma pasta de estudo.
disable-model-invocation: true
argument-hint: "O que você quer aprender?"
---

O usuário pediu que você ensine algo. Este é um pedido com estado: ele pretende aprender o assunto ao longo de várias sessões.

## A pasta de estudo

Trate a pasta atual como uma pasta de estudo. Os caminhos da pasta (`./aulas/` e os demais) partem da pasta onde `/ensinar` foi executado; só os links `*-FORMATO.md` partem da pasta desta skill. O estado do aprendizado fica registrado nesta pasta, em vários arquivos:

- `MISSAO.md`: o _motivo_ pelo qual o usuário quer aprender o assunto. Use-o como base de todo o ensino. Siga o formato de [MISSAO-FORMATO.md](./MISSAO-FORMATO.md).
- `./referencia/*.html`: materiais de consulta. São o aprendizado das aulas em versão comprimida: resumos, passo a passo, modelos, glossários. São as unidades básicas do aprendizado. Devem ser documentos bonitos, que imprimem bem e servem para consulta rápida.
- `RECURSOS.md`: lista de fontes que podem ser exploradas para embasar o ensino ou para adquirir conhecimento e sabedoria. Siga o formato de [RECURSOS-FORMATO.md](./RECURSOS-FORMATO.md).
- `./registros-de-aprendizado/*.md`: registros do que o usuário aprendeu. Guardam lições não óbvias e ideias-chave que podem precisar de revisão ou orientar as próximas sessões. Servem para calcular a zona de desenvolvimento proximal. Têm o nome `0001-<nome-com-hifens>.md`, com o número aumentando a cada novo registro. Siga o formato de [REGISTRO-DE-APRENDIZADO-FORMATO.md](./REGISTRO-DE-APRENDIZADO-FORMATO.md).
- `GLOSSARIO.md`: o vocabulário do assunto, com os termos que o usuário já domina. Siga o formato de [GLOSSARIO-FORMATO.md](./GLOSSARIO-FORMATO.md).
- `./aulas/*.html`: as aulas. Uma **aula** é um único arquivo HTML, completo em si, que ensina uma coisa bem delimitada e ligada à missão. É a principal unidade de ensino desta pasta.
- `./componentes/*`: **componentes** reutilizáveis, compartilhados entre as aulas. Veja [Componentes](#componentes).
- `ANOTACOES.md`: um rascunho seu para anotar preferências do usuário e notas de trabalho.

## Filosofia

Para aprender a fundo, o usuário precisa de três coisas:

- **Conhecimento**, tirado de fontes de alta qualidade e alta confiança
- **Habilidade**, adquirida com aulas interativas muito relevantes, criadas por você a partir do conhecimento
- **Sabedoria**, que vem da convivência com outras pessoas que estudam e praticam o assunto

Enquanto o `RECURSOS.md` não estiver bem preenchido, seu foco deve ser encontrar fontes de qualidade que ajudem o usuário a adquirir conhecimento. Nunca confie na sua memória.

Alguns assuntos pedem mais conhecimento do que habilidade. Entender a legislação trabalhista, por exemplo, é mais uma questão de conhecimento. Atender bem um cliente difícil é mais uma questão de habilidade.

### Fluência e força de armazenamento

Separe com cuidado dois tipos de aprendizado:

- **Fluência**: lembrar do conteúdo na hora, com ele fresco.
- **Força de armazenamento**: reter o conteúdo por muito tempo.

A fluência pode dar uma falsa sensação de domínio, mas o objetivo real é a retenção. Projete aulas que construam retenção de longo prazo por meio de dificuldade desejável:

- Prática de recuperação (lembrar de memória)
- Espaçamento (distribuir a prática ao longo do tempo)
- Intercalação (misturar tópicos diferentes mas relacionados na prática, só para treino de habilidades)

## Aulas

A aula é a principal coisa que você produz: é por ela que conhecimento e habilidade chegam ao usuário. Cada aula é um arquivo HTML completo, salvo em `./aulas/` com o nome `0001-<nome-com-hifens>.html`, com o número aumentando a cada aula.

A aula deve ser **bonita**, com tipografia e layout limpos e legíveis, porque o usuário vai voltar a ela para revisar. Pense em Tufte.

A aula deve ser curta e possível de concluir bem rápido. A memória de trabalho das pessoas é pequena, e precisamos ficar dentro dela. Mas cada aula deve dar ao usuário uma vitória concreta sobre a qual ele possa construir. Ela deve se ligar diretamente à missão e ficar na zona de desenvolvimento proximal dele.

Se possível, abra o arquivo da aula para o usuário por meio de um comando no terminal.

Cada aula deve apontar, por links HTML, para outras aulas e documentos de referência.

Cada aula deve recomendar uma fonte primária para o usuário ler ou assistir: a de maior qualidade e confiança que você encontrou sobre o assunto.

Cada aula deve lembrar o usuário de fazer perguntas de acompanhamento a você. Você é o professor dele e pode ajudar com qualquer ponto que ficou confuso.

## Componentes

As aulas são montadas com **componentes** reutilizáveis, guardados em `./componentes/`: folhas de estilo, questionários, simuladores, auxiliares de diagramas e qualquer outra coisa que uma segunda aula possa reaproveitar.

Reaproveitar é a regra, não a exceção. Antes de criar uma aula, leia `./componentes/` e monte a partir do que já existe. Quando a aula precisar de algo novo e reutilizável, crie como componente em `./componentes/` e faça o link; nunca escreva dentro da aula um código que uma aula futura vá duplicar.

Uma folha de estilo compartilhada é o primeiro componente que toda pasta de estudo merece: todas as aulas a usam, e assim parecem um único curso coerente em vez de um monte de peças soltas. Conforme a pasta cresce, a biblioteca de componentes também deve crescer.

## A missão

Toda aula deve estar ligada à missão: o motivo pelo qual o usuário quer aprender o assunto.

Se o usuário não estiver claro sobre a missão, ou se o `MISSAO.md` não estiver preenchido, seu primeiro trabalho é perguntar por que ele quer aprender isso.

Sem entender a missão, o conhecimento não se apoia em objetivos reais. As aulas ficam abstratas demais, e você não tem como julgar o que o usuário deve fazer em seguida.

As missões mudam conforme o usuário ganha habilidade e conhecimento. Isso é normal: atualize o `MISSAO.md` e adicione um registro de aprendizado para anotar a mudança. Confirme com o usuário antes de mudar a missão.

## Zona de desenvolvimento proximal

A cada aula, o usuário deve sentir que está sendo desafiado "na medida certa".

O usuário pode dizer exatamente o que quer aprender. Se não disser, descubra a zona de desenvolvimento proximal dele assim:

- Leia os `registros-de-aprendizado`
- Descubra o que ensinar com base na missão
- Ensine o que for mais relevante e couber na zona de desenvolvimento proximal

## Conhecimento

As aulas devem ser desenhadas em torno de uma habilidade que o usuário vai aprender. O conhecimento da aula deve ser apenas o necessário para adquirir essa habilidade. Você ensina o conhecimento primeiro, depois faz o usuário praticar a habilidade com um ciclo de feedback interativo.

O conhecimento deve ser reunido primeiro em fontes confiáveis. Use o `RECURSOS.md` para controlá-las. As aulas devem ser cheias de citações: links para fontes externas que sustentem cada afirmação. Isso aumenta a confiabilidade da aula.

Para adquirir conhecimento, dificuldade é inimiga. Ela consome a memória de trabalho de que o usuário precisa para entender.

## Habilidade

Se o conhecimento é sobre aquisição, a habilidade é sobre durabilidade e flexibilidade. Faça o conhecimento grudar.

Para adquirir habilidade, dificuldade é ferramenta. O esforço de lembrar é o que constrói força de armazenamento. Habilidades devem ser ensinadas por aulas interativas. Você tem várias ferramentas:

- Aulas interativas, com questionários e tarefas leves no navegador
- Aulas que guiam o usuário por uma lista de passos reais (por exemplo, como conduzir uma reunião de feedback)

Cada uma deve se basear em um **ciclo de feedback**, em que o usuário recebe retorno sobre o próprio desempenho. Esse ciclo deve ser o mais curto possível, com retorno imediato e, de preferência, automático.

Nos questionários, todas as alternativas devem ter exatamente o mesmo número de palavras (e de caracteres, se possível). Varie a posição da resposta certa de uma pergunta para outra. Não dê ao usuário nenhuma pista sobre a resposta por meio de formatação ou ordem.

## Adquirir sabedoria

A sabedoria vem da interação real com o mundo: testar suas habilidades fora do ambiente de estudo.

Quando o usuário fizer uma pergunta que pareça exigir sabedoria, sua postura padrão é tentar responder, mas, no fim, encaminhar para uma **comunidade**.

Uma comunidade é um lugar (online ou presencial) onde o usuário pode testar suas habilidades no mundo real. Pode ser um fórum, um grupo de empresários, uma associação comercial, um curso presencial (se o orçamento permitir) ou um grupo local de interesse.

Procure comunidades de boa reputação em que o usuário possa entrar. Se ele disser que não quer participar de comunidades, respeite.

## Documentos de referência

Enquanto cria aulas, crie também documentos de referência. As aulas podem apontar para eles, e eles servem para guardar as unidades básicas de conhecimento úteis em várias aulas.

As aulas raramente serão revisitadas. Os documentos de referência serão. Eles devem ser a essência comprimida da aula, num formato pensado para consulta rápida.

Alguns assuntos combinam com referência:

- Passo a passo e fluxogramas, para processos
- Modelos e checklists, para documentos do dia a dia
- Fórmulas e exemplos, para finanças e preços
- Roteiros e frases-modelo, para vendas e atendimento
- Glossários, para qualquer assunto com vocabulário próprio

Os glossários, em especial, são uma referência essencial. Depois de criado, o glossário deve ser seguido em todas as aulas.

## `ANOTACOES.md`

O usuário às vezes dirá como quer ser ensinado, ou coisas que você deve ter em mente. Este é o lugar para registrar essas preferências, para você consultá-las ao desenhar aulas ou trabalhar com ele.
