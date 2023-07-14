# Analise de risco da carteira de Ações

Neste projeto de Análise de Risco de Carteira com Ações, vamos analisar os cenários e uma cesta teórica de ações e como ela se comporta frente a critérios de Risco (vs) Retorno. Com isso, será possível proteger as rentabilidades e avaliar oportunidades e ameaças. Esta análise será feita em várias janelas temporais, com isso, será avaliado o grau de incertezas que essas janelas temporais oferecem à carteira de investimentos. Sabendo que quanto maior o tempo, maior é o risco de oscilação e por consequência um grau maior de volatilidade.

Quando falamos em gestão de risco são essenciais na identificação e na mitigação do risco de forma a proteger o capital investido. Podemos lembrar que cenários de guerra, pandemia entre outros afetam a performance dos ativos e a gestão do risco se faz necessário para quantificar possíveis perdas e até mesmo realocar ativos para uma carteira mais defensiva ou mais agressiva dependendo do cenário.

# Construção da Carteira
Através de uma interação do usuário em escolher o intervalo de datas e quais ações fará parte do portfólio e considerando pesos iguais. Na sequência, foi extraído os dados do Yahoo Finance considerando os preços ajustados de fechamento.







# Retornos
Considerando os retornos diários de cada ativo e na sequência fazendo uma limpeza do data frame com NaN. 

# Retorno do Portfólio
O retorno do portfólio, foi considerado a série de retornos multiplicado pelos pesos de cada ativo.

# Estatística descritiva.
Um quartil é qualquer um dos três valores que divide o conjunto ordenado de dados em quatro partes iguais, e assim cada parte representa 1/4 da amostra.
Assim, no caso de uma amostra ordenada:
primeiro quartil (designado por Q1/4) = quartil inferior = é o valor aos 25% da amostra ordenada = 25º percentil.
segundo quartil (designado por Q2/4) = mediana = é o valor até ao qual se encontra 50% da amostra ordenada = 50º percentil, ou  5º decil.
terceiro quartil (designado por Q3/4) = quartil superior = valor a partir do qual se encontram 25% dos valores mais elevados = valor aos 75% da amostra ordenada = 75º percentil à diferença entre os quartis superior e inferior chama-se amplitude inter-quartil.

Trazendo as informações de retorno do portfólio em um gráfico de histograma, será revelado no eixo y a frequência que o evento ocorre e no eixo x o intervalo de dispersão.

# Teoria moderna do portfólio - Markowtiz
A teoria do portfólio estabelece que decisões relacionadas à seleção de investimentos devam ser tomadas com base na relação risco-retorno. Para auxiliar neste processo, modelos de otimização de portfólio têm sido desenvolvidos. De modo a serem efetivos, tais modelos devem ser capazes de quantificar os níveis de risco e retorno dos investimentos.
Utilizando a teoria moderna de portfólio para o exemplo prático, podemos calcular a correlação dos ativos e no gráfico abaixo traz uma matriz evidenciando ativos que se correspondem com maior e menor relação.

# Calculando a Matriz de Covariância
Em teoria da probabilidade e na estatística, a covariância, ou variância conjunta, é uma medida do grau de interdependência (ou inter-relação) numérica entre duas variáveis aleatórias. Assim, variáveis independentes têm covariância zero. Ou seja, quanto mais próximo de um significa que são ativos que acompanham o mesmo movimento de mercado e quanto mais próximo de zero, menos têm relação entre si.

# Medindo a Volatilidade da Carteira
De acordo com a volatilidade com relação a pesos e covariância, podemos extrair as informações tanto diária, quanto anual.












# Calculando o Alfa da Carteira

Alfa é o termo usado nos investimentos para descrever a capacidade de um investimento render lucros acima do esperado no mercado.



# Calculando o Beta da Carteira
O Beta de um investimento indica se o investimento é mais ou menos volátil do que o mercado como um todo.
Beta é uma medida do risco decorrente da exposição a movimentos gerais de mercado em oposição a fatores peculiares. A carteira de mercado de todos os ativos investidos tem um beta de exatamente 1. Um beta abaixo de 1 pode indicar um investimento com menor volatilidade financeira do que o mercado, ou um investimento volátil cujos movimentos de preço não são altamente correlacionados com o mercado.


Em termos gerais, o beta da carteira mede o quanto ela se comporta em relação as variações do IBOVESPA. Logo abaixo, foi extraído este índice para fazer a comparação.

Neste código foi feito a junção dos dados.



# Value at Risk - VaR Histórico
O Value at Risk refere-se a um indicador de risco que considera a perda máxima possível de um investimento em um período de tempo e intervalo de confiança estabelecido. Para nossa simulação da carteira já virá calculado automaticamente pelos ativos e série temporal escolhida anteriormente.


Normalmente o VaR é calculado com 95%, 97,5% ou 99% de confiança. Este nível de confiança nos indica que é esperada perda maior que a calculada pelo VaR. Assim, ao utilizar 99% de confiança, espera-se que a cada 100 observações do VaR, em pelo menos 1 vez a perda do investimento financeiro seja superior à perda estimada no cálculo do VaR.
Através deste valor gerado pelo VaR, é possível fazer realocações da carteira para mitigação de riscos.
Por exemplo:
Em um VaR de 95% de intervalo de confiança, estima-se que 5% podem representar uma chance de risco de perda. Então, o investidor pode calcular o percentual da sua carteira através do código e redirecionar este valor para ativos de baixo risco.
Em um VaR de 98% de intervalo de confiança, estima-se que 3% podem representar uma chance de risco de perda. Então, o investidor pode calcular o percentual da sua carteira através do código e redirecionar este valor para ativos de baixo risco.
Em um VaR de 99% de intervalo de confiança, estima-se que 1% pode representar uma chance de risco de perda. Então, o investidor pode calcular o percentual da sua carteira através do código e redirecionar este valor para ativos de baixo risco.



Fontes: https://pt.wikipedia.org/, https://www.tradingcomdados.com.br/

