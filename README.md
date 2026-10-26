# Habilidades

Um conjunto de **habilidades (skills) para o Claude**, em português do Brasil, feitas para donos de negócio e para as pessoas que trabalham com eles. Você não precisa saber programar nem entender como a IA funciona por dentro.

## O que é uma habilidade?

É um conjunto de instruções que ensina o Claude a fazer uma tarefa do jeito certo, toda vez. Em vez de explicar do zero o que você quer ("escreve um e-mail para um cliente, mas educado, e não promete nada, e..."), você digita um comando curto, como `/responder-cliente`, e o Claude já sabe o roteiro: faz as perguntas certas, evita os erros comuns e guarda o resultado num arquivo.

## Para quem é

Para quem toca um negócio e quer usar o Claude no dia a dia sem virar especialista: planejar a semana, responder clientes, documentar processos, revisar preços, tomar decisões e escrever textos.

Se você está começando e não sabe por onde ir, digite `/primeiros-passos`. O Claude pergunta o que você quer resolver e aponta a habilidade certa.

## Instalação

Você precisa de uma conta do Claude **paga** (Pro, Max, Team ou Enterprise) para usar o Claude Code. O plano gratuito não inclui o Claude Code. O aplicativo de conversa do Claude sozinho não instala plugins: é preciso ter o **Claude Code**.

Escolha o seu caso:

- **Já uso o Claude Code:** vá para [Já tenho o Claude Code](#já-tenho-o-claude-code).
- **Só uso o aplicativo de conversa, ou o terminal não reconhece o `claude`:** siga a [Instalação guiada](#instalação-guiada-passo-a-passo).

### Já tenho o Claude Code

Abra uma conversa no Claude Code (por exemplo, na extensão do VS Code), digite os dois comandos abaixo, um de cada vez, e aperte Enter. Não precisa de terminal:

```text
/plugin marketplace add lucas-sachet/skills
/plugin install habilidades@lucas-sachet
```

Ou, pelo terminal:

```bash
claude plugin marketplace add lucas-sachet/skills
claude plugin install habilidades@lucas-sachet
```

Depois, abra uma **conversa nova** (plugins só carregam em conversas novas), numa pasta do seu negócio, e digite `/` seguido do nome da habilidade (por exemplo, `/primeiros-passos`). O Claude Code mostra a lista enquanto você digita.

### Instalação guiada, passo a passo

Cada passo diz **o que você deve ver** quando deu certo. Se não aparecer o esperado, pare e use a ajuda no fim desta seção.

**1. Abra o terminal.**
- Windows: aperte a tecla Windows, digite `PowerShell` e aperte Enter. A linha deve começar com `PS C:\`.
- Mac: aperte Command + Espaço, digite `Terminal` e aperte Enter.

**2. Instale o Claude Code.** Cole o comando do seu sistema e aperte Enter. Ele não mostra progresso, então espere até o cursor voltar.

Windows (PowerShell):

```powershell
irm https://claude.ai/install.ps1 | iex
```

Mac, Linux ou WSL:

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

**3. Feche o terminal e abra outro.** É necessário para o computador reconhecer o programa novo.

**4. Confira a instalação.**

```bash
claude --version
```

O esperado é aparecer um número de versão, como `2.1.211 (Claude Code)`.

Se aparecer *"claude não é reconhecido"* (Windows), o programa está instalado, mas a pasta dele não está no PATH. No PowerShell, confira se ele existe:

```powershell
Test-Path "$env:USERPROFILE\.local\bin\claude.exe"
```

Se mostrar `True`, adicione a pasta ao PATH, **feche o terminal e abra outro**, e repita o passo 4:

```powershell
$currentPath = [Environment]::GetEnvironmentVariable('PATH', 'User')
[Environment]::SetEnvironmentVariable('PATH', "$currentPath;$env:USERPROFILE\.local\bin", 'User')
```

Se mostrar `False`, a instalação do passo 2 não foi concluída: repita o passo 2. Se o terminal estiver dentro de um editor (como o VS Code), feche e abra o editor também.

**5. Entre na sua conta.** Digite `claude` e siga as instruções no navegador. Depois de entrar, digite `/exit` para sair.

**6. Instale as Habilidades.**

```bash
claude plugin marketplace add lucas-sachet/skills
claude plugin install habilidades@lucas-sachet
```

O esperado é ver *"Successfully installed plugin: habilidades@lucas-sachet"*. Para conferir, rode `claude plugin list`: a lista deve incluir `habilidades`.

**7. Comece a usar.** No terminal, vá até a pasta do seu negócio (`cd` seguido do caminho da pasta), digite `claude` e depois `/primeiros-passos`.

### Quer ajuda para fazer isso? Peça ao app do Claude

O aplicativo de conversa do Claude não consegue instalar por você (ele não tem acesso ao seu computador), mas pode **guiar você, passo a passo**, conferindo o que você colar de volta. Copie o texto abaixo, cole numa conversa do app e envie:

```text
Quero instalar o plugin "Habilidades" no Claude Code e preciso que você me guie, como um instrutor paciente. Eu não sei usar terminal.

Regras para você:
- Dê UM passo por vez e espere eu responder antes do próximo.
- Primeiro pergunte qual é o meu sistema (Windows, Mac ou Linux).
- Depois de cada passo, me diga o que eu devo ver na tela se deu certo e peça para eu colar aqui o que apareceu. Confira o que eu colar antes de seguir.
- Use linguagem simples. Se eu errar ou travar, explique o que aconteceu e o que fazer.
- Você não consegue rodar nada no meu computador: eu é que copio e colo os comandos.
- Use só os comandos abaixo e não invente outros. Se aparecer um erro que o roteiro não cobre, me peça para colar a mensagem inteira.

Roteiro:
1. Abrir o terminal. Windows: tecla Windows, digitar PowerShell, Enter (a linha começa com "PS C:\"). Mac: Command + Espaço, digitar Terminal, Enter.
2. Instalar o Claude Code. Windows PowerShell: irm https://claude.ai/install.ps1 | iex . Mac/Linux: curl -fsSL https://claude.ai/install.sh | bash . Não mostra progresso; esperar o cursor voltar. Aviso: precisa de uma conta paga do Claude (Pro, Max, Team ou Enterprise).
3. Fechar o terminal e abrir um novo.
4. Conferir: claude --version . Esperado: um número de versão. Se der "claude não é reconhecido" no Windows: rodar Test-Path "$env:USERPROFILE\.local\bin\claude.exe" . Se der True, rodar estes dois comandos: $currentPath = [Environment]::GetEnvironmentVariable('PATH', 'User') e depois [Environment]::SetEnvironmentVariable('PATH', "$currentPath;$env:USERPROFILE\.local\bin", 'User') , fechar o terminal, abrir outro e repetir a conferência. Se der False, refazer o passo 2.
5. Entrar na conta: digitar claude e seguir as instruções do navegador; depois digitar /exit.
6. Instalar as Habilidades: claude plugin marketplace add lucas-sachet/skills e depois claude plugin install habilidades@lucas-sachet . Esperado: "Successfully installed plugin: habilidades@lucas-sachet". Conferir com claude plugin list .
7. Usar: ir até a pasta do meu negócio, digitar claude e depois /primeiros-passos.

Comece agora, com a pergunta sobre o meu sistema.
```

### Se você já usa o Claude Code, mas o terminal não reconhece o `claude`

Cole o texto abaixo numa conversa do **Claude Code** (por exemplo, na extensão do VS Code), que tem acesso ao terminal do seu computador, e ele faz o trabalho por você:

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
