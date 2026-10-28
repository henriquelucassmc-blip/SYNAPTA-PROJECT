# SYNAPTA-PROJECT


- Candidato: Lucas Henrique Clemente Santos

- Etapa 1 do Projeto de Extensão SYNAPTA 

- Linguagem: Python


### Este projeto tem como objetivo analisar os preços de aluguéis de imóveis na cidade de São Paulo, buscando identificar características que estejam relacionadas aos valores cobrados, diferenças entre bairros e padrões presentes nos dados.


 Pergunta que orientou a análise: **Quais características parecem acompanhar os maiores e os menores preços de aluguel e o que os dados não permitem concluir?**


  ### O projeto utiliza um conjunto de dados sobre preços de aluguéis de imóveis em São Paulo, armazenado no arquivo data.csv:


**Plataforma:** Kaggle

**Dataset:** Preços de aluguéis em São Paulo

**Link:** [https://www.kaggle.com/datasets/renatosn/sao-paulo-housing-prices]

**Arquivo utilizado:** data.csv


O conjunto de dados original contém 11.657 registros e oito colunas.
Importante: o link exato do Kaggle não está identificado no notebook disponibilizado e precisa ser confirmado antes da publicação.



  #### Descrição das Colunas:

-> address:
 Endereço do imóvel

-> district:
 Bairro ou localidade do imóvel

-> area:
 Área do imóvel

-> bedrooms:
 Quantidade de quartos

-> garage:
 Quantidade de vagas na garagem

-> type:
 Tipo de imóvel

-> rent:
 Valor mensal do aluguel

-> total:
 Valor total informado, incluindo aluguel e demais custos



  #### Foram utilizadas as seguintes ferramentas:


<table>
  <tr>
    <td>python-dateutil</td>
    <td>numpy  </td>
    <td>et_xmlfile</td>
    <td>pandas</td>
    <td>six</td>
    <td>tzdata</td>
    <td>openpyxl</td>
  </tr>
  <tr>
    <td>3.0.0</td>
    <td>2.5.4</td>
    <td>2.0.0</td>
    <td>3.1.0</td>
    <td>1.17.0</td>
    <td>2026.5</td>
    <td>3.1.5</td>
  </tr>
</table>


 #### Como executar de forma correta para visualizar o projeto 

1. Acesse o Google Colab.

2. Envie o notebook Synapta_Projeto.ipynb.

3. Baixe o arquivo data.csv do Kaggle e envie-o ao Colab.

4. Execute as células do notebook na ordem.

5. Visualize os gráficos, as estatísticas e as conclusões da análise.

Para executar localmente, instale as dependências com **pip install -r requirements.txt**, abra o notebook no Jupyter e execute as células.
Observação: o arquivo **data.csv** deve estar no caminho indicado pelo código.


   #### A preparação dos dados foi realizada antes dos cálculos e da criação dos gráficos:

**Carregamento:** leitura do arquivo data.csv utilizando Pandas.
**Inspeção inicial:** verificação das colunas, quantidade de registros e tipos de dados.
**Valores ausentes:** análise da quantidade de valores preenchidos em cada coluna. Na inspeção inicial, todas as colunas apresentaram 11.657 valores não nulos.
**Duplicatas:** identificação e remoção de registros com endereços repetidos, considerando a coluna address.
**Área dos imóveis:** manutenção dos registros cuja área é maior que zero.
**Valores numéricos:** verificação de áreas, quartos, vagas, aluguéis e valores totais para identificar possíveis inconsistências.
**Valores atípicos:** remoção dos registros com aluguel superior a R$ 15.000.
**Análise estatística:** cálculo da média, mediana, preços médios por bairro e correlações entre variáveis.

As transformações foram realizadas diretamente no DataFrame utilizado pela análise. A quantidade final de registros deve ser consultada após a execução de todas as etapas.


A limpeza e preparação de dados de forma resumida foi: Verificação de valores ausentes, remoção de endereços duplicados, exclusão de imóveis com área inválida (menor ou igual a zero) e remoção de aluguéis acima de R$ 15.000. Em seguida, os dados foram organizados para calcular estatísticas, comparar bairros e analisar correlações entre as variáveis.


   #### Principais Conclusões: 

1.  **A diferença entre a Média e a Mediana:** O preço médio dos aluguéis foi de aproximadamente 3.028,34, enquanto a mediana foi de 2.250,00. Isso indica que os aluguéis mais elevados aumentam a média.

2. **Relação entre os alugueis com a área dos imóveis:** A correlação de aluguel com a área foi de 0,70, indicando uma relação positiva relativamente forte. Em geral, imóveis com áreas maiores tendem a apresentar aluguéis mais elevados.

3. **Relação entre os aluguéis com a quantidade de quartos dos imóveis:** A correlação de quartos com aluguel foi de 0,57, indicando uma relação positiva moderada. Imóveis com mais quartos tendem a apresentar aluguéis maiores, embora essa relação seja menos intensa do que a observada com a área.

4. **Bairros com maiores preços médios:** Entre as localidades analisadas com pelo menos 30 registros, Campo Belo apresentou o maior preço médio, de aproximadamente R$ 4.964,08 por mês.

5. **Bairros com menores preõs médios:** Entre as localidades que atenderam ao mesmo critério, Liberdade apresentou o menor preço médio, de aproximadamente R$ 1.791,30 por mês. A diferença em relação a Campo Belo evidencia variações relevantes entre os bairros analisados.



  #### Algumas limitações da análise:

1. **Ausência de informações:** O conjunto de dados não apresenta todos os fatores que podem influenciar o aluguel, como: ***estado de conservação do imóvel, mobiliário, condomínio e proximidade de serviços.***

2. **Concentração dos anúncios:** A quantidade de anúncios varia entre os bairros analisados. Por isso, os resultados de bairros com menos registros podem ser menos representativos.

3. **Preços anunciados:** Os valores representam os preços informados nos anúncios, que podem ser **diferentes dos valores** efetivamente negociados entre proprietários e inquilinos.

4. **Exclusão de registros:** A análise removeu endereços repetidos e anúncios com aluguel superior a R$ 15.000. Essa decisão pode ter excluído imóveis **válidos e influenciado as médias calculadas.**

5. **Dados inconsistentes:** Foram identificados valores de área iguais a zero e registros com zero quartos, que precisam ser verificados para evitar distorções nos resultados.

6. **Correlação não significa causalidade:** Embora a área tenha apresentado correlação positiva com o aluguel, isso não significa que ela seja a única responsável pelo aumento dos preços.


Houve a utilização de IA inteligência Artificial Generativa somente para formulação de perguntas sobre o código, escrita e pesquisa relacionadas a conclusões e limitação de análise.



  #### Imagens de alguns gráficos utilizados no código:

<div align="center">
<img width="600" height="456" alt="Image" src="https://github.com/user-attachments/assets/091df723-dc24-469c-bdd6-67268377be25" />
</div>  


<div align="center">
<img width="578" height="541" alt="Image" src="https://github.com/user-attachments/assets/abffc3dd-7dfe-4ae2-9db9-ce7eeef2fd1e" />
</div>


<div align="center">
<img width="576" height="566" alt="Image" src="https://github.com/user-attachments/assets/524079fb-82dd-4df5-846c-48e9386c87a1" />
</div>
