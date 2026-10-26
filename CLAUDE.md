# Habilidades

Skills do Claude em português (BR) para donos de negócio e suas equipes, sem exigir conhecimento técnico. Adaptado de [mattpocock/skills](https://github.com/mattpocock/skills) (MIT).

## Regras

- Cada skill fica em `skills/<nome>/SKILL.md`, sem subpastas de categoria.
- Toda skill nova ou renomeada entra na lista `skills` de `.claude-plugin/plugin.json` e na tabela do `README.md`.
- `primeiros-passos` guarda o mapa de qual skill usar em cada situação. Ao adicionar, renomear ou remover uma skill, atualize esse mapa.
- Escreva em português do Brasil, em linguagem simples: sem jargão de programação, com exemplos de negócio (clientes, vendas, equipe, processos).
- Sem travessão (—) na prosa. Use vírgula, dois-pontos, ponto ou parênteses.
- Rode `claude plugin validate . --strict` depois de mexer em qualquer manifesto.
