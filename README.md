# 🧠 TSE Analytics - Eleições 2024
Análise dos dados das eleições 2024.

## 👀 Visão Geral do Projeto: 
O dataset foi gerado por Teo Calvo em suas lives da Twitch a partir dos dados do TSE 2024. 
Os dados buscam mostrar a representatividade das pessoas pretas, pardas, não brancas e do gênero feminino na política brasileira.
Contando com dimensões como idade, média de bens e estado civil, os dados buscam caracterizar os personagens da política brasileira para as eleições de vereador, vice-prefeito e prefeito.

## 🕵️ Preparação dos Dados: 
- Os dados foram importados via CSV e tratados via Power Query.
- Foram excluidas as linhas da coluna DS_CARGO que possuíam o Valor "Geral" por se tratar de um agregado dos dados.
- Foram excluídas as linhas da coluna SG_UF que continham o valor "BR" por se tratar de um agregado da somatória dos estados.
- O dataset foi dividido em 3 tabelas.
  - **dim_partidos** :
      - colunas:
          - NM_PARTIDO : Tipo texto, que contem os nomes dos partidos.
          - SG_PARTIDO: Tipo texto, que contém as siglas dos partidos.
  - **dim_estados** :
      - Colunas:
          - SG_UF: Tipo texto, que contém a siglas dos estados do Brasil.
          - UF_FULL: Tipo texto, que contém o nome dos estados brasileiros.
  - **tse_fato** :
      - Colunas:
          - avg_Bens: Número decimal, categoria moeda, que contem a média dos bens dos candidatos por estado.
          - abgBensNotZero: Número decimal, categoria moeda, que contém a média dos bens dos candidatos sem levar em consideração os valores 0.
          - avdIdade: Número inteiro, média de idade dos candidadatos por estado.
          - DS_CARGO: Tipo texto, que contém a descrição dos cargos.
          - SG_PARTIDO: Tipo texto, que contém a sigla dos partidos.
          - SG_UF: tipo texto, que contém a sigla dos estados brasileiros.
          - totalBens: número inteiro, que contém a somatória dos bens declarados pelos candidatos por estado.
          - totalCandidaturas: tipo inteiro, total de candidaturas por estado e por cargo.
          - totalCorRaçaNaoBranca: tipo inteiro, total de candidaturas por estado e por cargo de pessoas que declararam como Raça Não Branca.
          - totalCorRaçaPreta: tipo inteiro, total de candidaturas por estado e por cargo de pessoas que declararam como Raça Preta.
          - totalCorRaçaPretaParda: tipo inteiro, total de candidaturas por estado e por cargo de pessoas que declararam como Raça Preta/Parda.
          - totalGenFeminino: tipo inteirom, total de candidaturas por estado e por cargo de pessoas que declararam como Gênero feminino.
          - txCorRaçaNaoBranca: tipo número decimal,  porcentagem de candidatos por estado e por cargo de pessoas que declararam como Raça Não Branca.
          - txCorRaçaPreta: tipo número decimal,  porcentagem de candidatos por estado e por cargo de pessoas que declararam como Raça Preta.
          - txCorRaçaPretaParda: tipo número decimal,  porcentagem de candidatos por estado e por cargo de pessoas que declararam como Raça Preta.
          - txGenFeminino: tipo número decimal,  porcentagem de candidatos por estado e por cargo de pessoas que declararam como Gênero Feminino.
          - txEstadoCivilCasado: tipo número decimal,  porcentagem de candidatos por estado e por cargo de pessoas que declararam estado civil casado.
          - txEstadoCivilSeparadoDivorciado: tipo número decimal,  porcentagem de candidatos por estado e por cargo de pessoas que declararam estado civil separado/divorciado.
          - txEstadoCivilSolteiro: tipo número decimal,  porcentagem de candidatos por estado e por cargo de pessoas que declararam estado civil solteiro.


## 🔬 Análise dos Resultados:

## Evolução & Próximos Passos: 
