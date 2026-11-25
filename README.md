# Calculadora Renda Fixa Focus — versão 1.0

Versão independente da Calculadora Renda Fixa, com identidade visual roxa.

**Idealizador:** Marcelo Amendola.

## Premissas da versão 1.0

- Selic inicial editável pelo usuário; o CDI inicial é calculado como Selic menos 0,10 ponto percentual.
- Projeções de Selic para dezembro fixas, conforme a mediana do Boletim Focus de 23/11/2026:
  - Dezembro/2026: 13,75% a.a.
  - Dezembro/2027: 13,00% a.a.
  - Dezembro/2028: 11,00% a.a.
  - Dezembro/2029: 10,50% a.a.
- O modelo considera oito reuniões do COPOM por ano. As alterações são distribuídas ao longo das reuniões em passos de 0,25 ponto percentual, com ajuste residual apenas se necessário para atingir exatamente a projeção de dezembro.
- A decisão de cada reunião passa a valer no mês seguinte, como aproximação para a capitalização mensal.
- CDI projetado = Selic projetada menos 0,10 ponto percentual.
- A taxa anual é convertida em taxa efetiva mensal equivalente e capitalizada de forma composta, mês a mês.
- O usuário informa o prazo em meses e a rentabilidade contratada em percentual do CDI.
- A equivalência entre LCA/LCI e CDB é resolvida numericamente, comparando os montantes finais líquidos após IR do CDB.
- A alíquota de IR do CDB segue a tabela regressiva, usando o prazo informado em meses convertido em períodos de 30 dias.
- Para prazos além de dezembro/2029, mantém-se a Selic terminal projetada de 10,50% a.a.

## Fontes

- Banco Central do Brasil, Relatório Focus de 23/11/2026: https://www.bcb.gov.br/content/focus/focus/R20261123.pdf
- Banco Central do Brasil, calendário de reuniões do COPOM de 2027 (Comunicado nº 45.452, de 23/06/2026): https://www.bcb.gov.br/estabilidadefinanceira/exibenormativo?numero=45452&tipo=Comunicado

As projeções são expectativas de mercado e não garantias de taxas futuras. O cronograma mensal de reduções é uma hipótese de simulação da calculadora, não uma previsão oficial de decisões do COPOM.

Não é recomendação de investimento.


Atualização de publicação: commit de disparo do workflow GitHub Pages.
