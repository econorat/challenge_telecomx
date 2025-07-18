Análise e Previsão de Evasão de Clientes (Churn) em Telecomunicações

🎯 Introdução
Este repositório contém um estudo aprofundado sobre a evasão de clientes (Churn) em uma empresa de telecomunicações. O objetivo principal é identificar os principais fatores que levam os clientes a cancelar seus serviços, fornecendo insights acionáveis e recomendações estratégicas para reduzir a taxa de Churn e melhorar a retenção de clientes.

A evasão de clientes é um desafio significativo para qualquer negócio de serviço, pois a aquisição de novos clientes é, em geral, mais custosa do que a retenção dos clientes existentes. Compreender por que os clientes saem é o primeiro passo para construir um modelo de previsão e, mais importante, para desenvolver intervenções eficazes.

🚀 Objetivo do Projeto
Identificar Padrões de Churn: Analisar a distribuição da variável Churn e como ela se comporta em relação a diferentes características dos clientes.

Explorar Fatores Chave: Descobrir quais variáveis categóricas (ex: tipo de contrato, serviços adicionais) e numéricas (ex: tempo de permanência, gastos mensais) estão mais fortemente associadas à evasão.

Gerar Insights Acionáveis: Fornecer conclusões claras e recomendações práticas que a empresa possa implementar para mitigar o Churn.

📊 Dados
O dataset utilizado (TelecomX_Data.json) contém informações detalhadas sobre clientes de uma empresa de telecomunicações, incluindo:

Informações do Cliente: Gênero, se é idoso, se tem parceiro ou dependentes.

Informações dos Serviços: Serviço telefônico, múltiplas linhas, tipo de serviço de internet, serviços de segurança online, backup online, proteção de dispositivo, suporte técnico, streaming de TV e filmes.

Informações da Conta: Tempo de permanência (Tenure), tipo de contrato, fatura digital, método de pagamento, cobranças mensais (MonthlyCharges) e cobranças totais (TotalCharges).

Variável Alvo: Churn (indica se o cliente evadiu ou não).

🛠️ Metodologia
O estudo foi dividido nas seguintes etapas:

Carregamento e Limpeza de Dados:

Importação do arquivo JSON para um DataFrame Pandas.

Tratamento de valores ausentes e inconsistências (TotalCharges, Churn).

Criação de novas variáveis (DailyCharges, NumServices).

Conversão de variáveis categóricas para um formato numérico binário (0/1) para facilitar a análise.

Padronização dos nomes das colunas.

Análise Exploratória de Dados (EDA):

Visualização da distribuição geral do Churn para entender a proporção de clientes que evadem.

Análise da relação do Churn com variáveis categóricas utilizando gráficos de barras empilhados (ex: Contract, InternetService, PaymentMethod, serviços adicionais).

Análise da relação do Churn com variáveis numéricas utilizando box plots e histogramas/gráficos de densidade (ex: Tenure, MonthlyCharges, TotalCharges, DailyCharges).

Cálculo e visualização da matriz de correlação para identificar as relações lineares entre todas as variáveis numéricas e, especialmente, com o Churn.

🔍 Análise e Insights Chave
A análise exploratória revelou os seguintes padrões críticos relacionados à evasão:

Alto Risco em Contratos Mês a Mês: Clientes com contrato mês a mês apresentam uma taxa de Churn drasticamente maior (~42.7%) em comparação com contratos de um e dois anos.

Clientes Novos São Mais Vulneráveis: Clientes com baixo tempo de permanência (Tenure) são significativamente mais propensos a evadir. A evasão é mais comum nos primeiros meses de serviço.

Impacto dos Serviços de Internet e Custo: Clientes que utilizam Fibra Óptica e têm cobranças mensais mais altas demonstram maior tendência a sair. Isso pode indicar problemas de qualidade de serviço ou percepção de custo-benefício.

Método de Pagamento de Alto Risco: O Cheque Eletrônico é o método de pagamento associado à maior taxa de Churn (~45.3%).

Serviços Adicionais como Retentores: Clientes que NÃO possuem serviços de segurança online (OnlineSecurity) e suporte técnico (TechSupport) são mais propensos ao Churn. Aumentar o número de serviços adicionais contratados diminui significativamente a probabilidade de evasão.

Perfis Específicos: Clientes idosos e aqueles sem parceiros ou dependentes também exibem uma leve tendência a churnar mais.

💡 Recomendações Estratégicas
Com base nos insights obtidos, sugerimos as seguintes ações para a empresa:

Focar na Retenção de Clientes Novos:

Implementar um programa de onboarding robusto para novos clientes.

Oferecer incentivos para contratos de longo prazo (descontos, bônus) nos primeiros meses de serviço.

Realizar acompanhamento proativo da satisfação dos clientes nos primeiros 6-12 meses.

Otimizar o Serviço de Fibra Óptica:

Investigar a qualidade do serviço e o suporte técnico para usuários de Fibra Óptica.

Considerar pesquisas de satisfação específicas para este segmento.

Reavaliar Planos de Alto Custo:

Analisar a competitividade dos planos com cobranças mensais elevadas.

Considerar o ajuste de preços ou a adição de benefícios para justificar o valor percebido.

Promover Serviços de Segurança e Suporte:

Realizar campanhas de marketing destacando os benefícios de OnlineSecurity e TechSupport.

Considerar a inclusão desses serviços em pacotes ou a oferta de descontos para incentivar a adesão.

Analisar o Método de Pagamento (Cheque Eletrônico):

Investigar o perfil e a satisfação dos clientes que utilizam Cheque Eletrônico.

Explorar a possibilidade de incentivar a mudança para métodos de pagamento mais estáveis e menos associados ao Churn.

Desenvolver Programas de Fidelidade:

Criar programas que recompensem clientes de longa data, incentivando um maior Tenure e fortalecendo a lealdade.
