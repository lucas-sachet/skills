---
name: revisar-oferta
description: Revisa a oferta e o preço de um produto ou serviço (o que é vendido, por quanto, para quem e como é apresentado), faz as contas de margem e ponto de equilíbrio, aponta o que atrapalha a venda e sugere testes pequenos. Use quando o usuário falar em "preço", "precificar", "minha oferta", "proposta comercial", "promoção", "vendo pouco" ou "estou cobrando certo?".
---

Ajude o usuário a enxergar a própria oferta como um cliente enxerga e a conferir se o preço sustenta o negócio. Você **não decide o preço**: mostra as contas, aponta problemas, compara alternativas e recomenda com o motivo. A decisão é do usuário.

## Passos

1. **Colete os dados em uma só mensagem.** Peça, com respostas curtas aceitas:
   - O que você vende, para quem e que problema resolve?
   - Quanto cobra hoje, e como o preço é apresentado ao cliente?
   - Quanto custa produzir ou entregar **uma unidade** (material, mão de obra direta, comissão, frete, taxas e impostos sobre a venda)?
   - Quais são os custos fixos do mês (aluguel, salários, ferramentas, contador)?
   - Quantas vendas por mês hoje, e quantas você precisaria?
   - Quem são os concorrentes ou alternativas do cliente, e quanto cobram (se souber)?
   - Que reações você ouve sobre o preço ("está caro", "vou pensar")?

   Se faltar um número, não chute: diga qual falta e o que ele mudaria na análise. Está pronto quando existe preço, custo por unidade e pelo menos uma ideia do cliente-alvo.

2. **Faça as contas e mostre a conta.** Use só os números informados e indique a fórmula:
   - **Margem de contribuição** = preço − custos que variam com cada venda. Em porcentagem: margem ÷ preço.
   - **Ponto de equilíbrio** = custos fixos do mês ÷ margem de contribuição por unidade (quantas vendas por mês para empatar).
   - **Quanto o preço pode cair** antes de a margem acabar, e quanto ele teria que subir para chegar a uma margem desejada pelo usuário.

   Avise que são estimativas feitas com os dados dados, e que impostos e regime tributário devem ser confirmados com o contador.

3. **Olhe a oferta por cinco lentes.** Para cada uma, diga se está ok ou se é um problema, com a evidência da própria conversa:
   - **Clareza:** o cliente entende em dez segundos o que recebe, para quem é e por que custa isso?
   - **Valor:** a oferta fala do resultado para o cliente (mais tempo, menos erro, mais vendas) ou só lista características?
   - **Preço:** cobre custos e deixa margem? Está fora do padrão das alternativas sem uma razão que o cliente enxergue? Há pacotes ou opções (básico, completo) que ajudam o cliente a escolher?
   - **Risco:** o que o cliente teme perder ao comprar, e a oferta reduz esse medo (garantia, teste, prazo para desistir, prova de quem já comprou)?
   - **Próximo passo:** fica óbvio como comprar ou pedir uma proposta, e até quando a oferta vale? Urgência só se for real: não invente escassez ou prazo.

4. **Entregue o diagnóstico, do mais importante para o menos.** Para cada problema: o que você viu, por que atrapalha a venda, uma sugestão concreta e **um teste pequeno** para verificar (por exemplo, "por duas semanas, apresente o pacote completo primeiro e meça quantos escolhem o básico"). Diga o que NÃO dá para concluir com os dados atuais.

5. **Mostre 2 ou 3 alternativas de oferta**, cada uma com suas vantagens e riscos e o efeito nas contas (nova margem e novo ponto de equilíbrio). Faça uma recomendação e diga em que situação ela estaria errada.

6. **Ofereça pesquisar o mercado.** Se faltarem preços de concorrentes ou referências do setor, ofereça usar a skill `pesquisar` em vez de adivinhar. Se o usuário aceitar, cite as fontes na revisão.

7. **Salve a revisão** em `revisao-oferta-<nome>.md` na pasta atual, com os dados usados, as contas, o diagnóstico, as alternativas e os testes combinados. Ao fim, pergunte qual teste o usuário quer fazer primeiro e quando vão olhar o resultado.

## Cuidados

- **Nunca invente números** de mercado, concorrentes ou resultados esperados. Prometer "isso vai aumentar suas vendas em 30%" é inventar.
- **Promoções, descontos, garantias e propaganda** têm regras (como o Código de Defesa do Consumidor). Se a sugestão mexer nisso, avise o usuário para confirmar com um profissional.
- **Preço baixo não é a única saída.** Antes de sugerir baixar, veja se o problema é clareza, valor ou risco.
- **Não decida por ele.** Se o usuário pedir "diga o preço certo", devolva uma faixa com as contas e o motivo, e deixe claro o que depende do conhecimento dele sobre o próprio cliente.
