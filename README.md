# Projeto de Previsão e Análise de Consumo Energético com Tomadas Inteligentes B.I.N.

## Link para o vídeo no YouTube:
https://youtu.be/7Ru1AD7ZKDQ

## Descrição do Problema
O consumo energético residencial é um dos principais fatores que impactam tanto as contas de luz quanto o meio ambiente. Este projeto tem como objetivo conscientizar as pessoas sobre o uso de energia, utilizando um protótipo de tomada inteligente capaz de medir o consumo em tempo real e oferecer insights práticos.

Com base nos dados capturados, buscamos responder às seguintes questões:
1. O consumo diário atual pode levar a ultrapassar a média mensal de 152,2 kWh de uma residência brasileira?
2. O consumo energético ao longo dos meses está aumentando, diminuindo ou permanecendo estável?

## Metodologia
### Coleta de Dados
- Simulação de um dataset com 500 registros, representando o consumo diário, mensal e histórico de diferentes cômodos de residências brasileiras.
- Incluídos dados históricos de consumo energético de junho a novembro de 2024.
- Tenha em mente que o protótipo gera os mesmos dados utilizados no dataset mockup, mas para termos mais dados decidimos gerar.

### Modelagem
Dois modelos principais foram desenvolvidos, ambos utilizando redes neurais artificiais com o framework Keras:

1. **Modelo 1: Previsão de Ultrapassagem do Consumo Médio Mensal**  
   Este modelo utiliza o consumo diário (`Watt-dia`) para prever se o consumo mensal total do usuário ultrapassará a média nacional de 152,2 kWh/mês.  
   - Arquitetura: Rede neural com 3 camadas densas e ativação Sigmoid para classificação binária.
   - Desempenho: Aproximadamente **85% de acurácia** no conjunto de teste.

2. **Modelo 2: Análise de Tendências de Consumo**  
   Este modelo analisa o histórico de consumo mensal (de junho a outubro) para prever se o consumo aumentará em novembro.  
   - Arquitetura: Rede neural com 3 camadas densas e ativação Sigmoid para classificação binária.
   - Desempenho: Aproximadamente **88% de acurácia** no conjunto de teste.

### Pré-Processamento
- Normalização dos dados de entrada com `StandardScaler` para uniformizar as escalas.
- Divisão dos dados em conjuntos de treinamento (80%) e teste (20%).
- Geração de variáveis derivadas, como mudanças de consumo mensal, para análise de tendências.

### Ferramentas Utilizadas
- **Manipulação de Dados**: Pandas
- **Machine Learning**: TensorFlow, Keras, Scikit-learn
- **Visualização**: Matplotlib, Seaborn

## Resultados
Os modelos geraram insights práticos para conscientização e gerenciamento do consumo energético:

1. **Previsão de Ultrapassagem do Consumo Médio**  
   Usuários podem receber alertas sobre o risco de ultrapassagem da média mensal, ajudando a evitar aumentos na conta de luz.

2. **Análise de Tendências**  
   Identificação de padrões de aumento, redução ou estabilidade no consumo ao longo dos meses, permitindo ajustes comportamentais e identificação de desperdícios.

3. **Visualizações e Conscientização**  
   - Gráficos mostram a sazonalidade e o impacto de diferentes cômodos no consumo total.
   - Dados históricos incentivam os usuários a adotar práticas mais sustentáveis.

## Conclusões
Este projeto destaca como a tecnologia pode ser utilizada para promover eficiência energética e conscientização. Os principais pontos incluem:
- A tomada inteligente serve como uma ferramenta valiosa para monitorar o consumo e gerar insights em tempo real.
- Os modelos de machine learning oferecem previsões confiáveis e auxiliam na gestão do consumo energético.
- A conscientização sobre o uso de energia é fundamental para reduzir custos e impacto ambiental.

## Com isto podemos
- Desenvolver um aplicativo móvel para apresentar insights aos usuários de forma interativa.
- Expandir o dataset com dados reais para validar os modelos e aprimorar as previsões.
- Implementar notificações e dicas personalizadas para promover hábitos de consumo mais conscientes.
