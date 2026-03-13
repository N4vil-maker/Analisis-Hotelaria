# Projeto de Consumo e Sazonlnalidade Hoteleira
Este projeto analisa o comportamento das reservas e da faturacao de dois hotéis, (City e Resort), com foco na limpeza de dados, segmentacao e deteccao de valores atípicos (outliers)

#Processamento e Limpeza de Dados
Para garantir uma análise rigorosa, realizei as seguintes ações de Data Wrangling

Filtragem de ADR: Eliminação de registros com tarifas incorretas (menores que 0 ou maiores que 1000) para evitar distorções na media (mean).
Integridade de Hóspedes: Criei uma coluna da suma total de personas ( adultos, criancas e bebes). Identifiquei e Invalidei reservas com valores nulos (0).
Metricas de Receita (Inteligencia de negocios): Criei de uma nova coluna 'df_revenue',  multiplicando 'adr' por 'total_nights'. Considerando reservas unicamente com Check-out.

#Principais descobertas (Insights)

Perfil de Clientes: Segum os quartis (25%, 50%, 75%) o perfil predominante é de casais (2 adultos) sem criancas.
Seazonalidade: O pico de faturamento consentra-se no mes de agosto, embora julho apresente alta densidade de noites hospedadas.
Detecção de Outliers: Identifiquei uma reserva atípica de nacionalidade italiana (ITA) com um ADR de $510, valor muito superior à média de $103,48, mesmo para uma categoria de quarto simples (A).

#Visualização
Utilizei Seaborn e Matplotlib para representar:
Lineplot: Tendência de receita mensal (ordenada cronologicamente de janeiro a dezembro através de categorias).
Barplot: Ranking de receita por país de origem (Top 10) segmentado por tipo de hotel.

#Próximos Passos
Finalizar a integração dos dados limpos no Power BI para criação de dashboards dinâmicos.

