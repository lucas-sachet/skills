# Formato do registro de aprendizado

Os registros de aprendizado ficam em `./registros-de-aprendizado/` e usam numeração sequencial: `0001-nome.md`, `0002-nome.md` e assim por diante. Crie a pasta só quando escrever o primeiro registro.

Eles guardam lições não óbvias, ideias-chave e conhecimento prévio declarado, que vão orientar as próximas sessões. Servem para calcular a zona de desenvolvimento proximal.

## Modelo

```md
# {Título curto do que foi aprendido ou estabelecido}

{1 a 3 frases: o que foi aprendido (ou que conhecimento prévio foi estabelecido) e por que isso importa para as próximas sessões.}
```

Esse é o formato inteiro. Um registro pode ser um único parágrafo. O valor está em anotar _que_ isso agora é conhecido e _por que_ isso muda o que ensinar depois, não em preencher seções.

## Seções opcionais

Inclua só quando agregarem valor de verdade. A maioria dos registros não precisa delas.

- **Status** no início (`ativo | substituído por RA-NNNN`): útil quando um entendimento anterior se mostra errado e é trocado.
- **Evidência**: como o usuário demonstrou o entendimento (uma pergunta respondida, um exercício concluído, uma experiência citada). Útil quando a afirmação pode ser revista.
- **Implicações**: o que isso libera ou descarta nas próximas sessões. Vale registrar quando não for óbvio.

## Numeração

Veja o maior número existente em `./registros-de-aprendizado/` e some um.

## Quando escrever um registro

Escreva um quando qualquer uma destas for verdade:

1. **O usuário demonstrou entendimento real de algo não trivial**: não só contato com o tema, mas prova de que sabe usar o conceito corretamente. Isso cria um novo piso para o que ensinar a seguir.
2. **O usuário revelou conhecimento prévio**: "eu já sei X". Registre, para as próximas sessões não ensinarem de novo. Registre também a _profundidade_ declarada.
3. **Um equívoco foi corrigido**: o usuário acreditava em algo errado e agora entende o porquê. Esses são os mais valiosos: antecipam tropeços em temas parecidos.
4. **A missão mudou por causa do aprendizado**: o usuário descobriu que se importa com algo diferente do que pensava. Faça o link para [[MISSAO.md]] e atualize-o.

### O que _não_ merece registro

- Conteúdo que apenas foi coberto. Cobrir não é aprender. Espere a evidência.
- Qualquer coisa já registrada de forma enxuta como definição no [[GLOSSARIO.md]]. Não duplique.
- Diários de atividade sessão a sessão. Registros de aprendizado não são um diário: são aprendizados com peso de decisão.

## Substituição

Quando um registro posterior contradiz um anterior (o entendimento do usuário se aprofundou ou foi corrigido), marque o antigo como `Status: substituído por RA-NNNN` em vez de apagá-lo. A história de como o entendimento evoluiu é um sinal útil.
