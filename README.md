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

### **Visão Geral**
- 458.97 mil candidatos concorrem aos cargos de Prefeito, Vice-prefeito e Vereador em todo o Brasil.
- 242.98 mil candidatos declaram serem de raça preta/parda.
- 52.26 mil candidatos declararam serem de raça Preta.
- 249.42 mil candidatos declararam serem de raça não branca.
- São Paulo é o estado com maior número de candidatos aos cargos.
- O estado com maior representatividade de candidatos de raça preta é a Bahia também sendo o 3 maior em número de candidatos, enquanto o menor é o Rio Grande do Sul com 4.81%.
- Amapá tem a maior taxa de candidatos de raça não branca e preta/parda.

### **Visão Partidos**
- MDB é o partido com maior número de candidatos com 44.086 mil candidatos.
- O partido com menor número de candidatos é o PCB.
- O partido com mais bens declarados é também o MDB com 191.057.604,56 bilhões declarados, partido esse conhecido por ser o partido dos super ricos.
- O partido com menos bens declarados é o PCO com 1.833.602,53 milhões declarados em todo país.
### **Visão Candidatos**
- A média de idade dos candidatos é 48 anos.
- A média dos candidatos declararam estado civil casado é de 53%.
- 0.61% dos candidatos declararam estado civil separado/divorciado.
- 35% dos candidatos declararam estado civil solteiro.
- 27% dos candidatos declararam ser do gênero feminino.
- **Relação Idade/Estado Civil/ Partido:
  - O partido que possui a menor média de idade é o UP (Unidade Popular), com média de idade de 36 anos.
  - o partido com mais candidatos solteiros (86%) e do gênero feminino(55%) é o UP (Unidade Popular).
  - O partido com maior média de candidatos casados é o PL com 62% dos candidatos declarados como casados.
  
## Evolução & Próximos Passos: 
- Elaboração de um algoritmo de clusterização para definir a proximidades dos partidos de acordo com essas características e cruzar com seus alinhamentos políticos.

## Link do Projeto:
![Link]https://app.powerbi.com/view?r=eyJrIjoiZWNjNzFlNjEtZTVmYy00OWIwLThkYTctN2Q3NjI1YjdiNmFjIiwidCI6IjQyOTJlZGZlLTcxN2QtNDgxYy1hZmQwLWUwNWU3NzJiNjhiMiJ9&pageName=b8c756e0130a9a90d7fe
