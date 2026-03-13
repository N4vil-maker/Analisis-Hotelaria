# Projeto de Consumo e Sazonlnalidade Hoteleira #Work in Progress

Fase de limpeza de dados e EDA concluída; próximos passos: visualização
Este projeto analisa os padrões de reservas e receitas de dois hotéis (City e Resort), com foco na limpeza de dados, segmentação e detecção de outliers

#Processamento e Limpeza de Dados
Para garantir uma análise rigorosa, realizei as seguintes tarefas de preparação de dados

Filtragem de ADR: Removi registros com tarifas incorretas (menores que 0 ou maiores que 1000) para evitar distorções na média.
Integridade dos hóspedes: Criei uma coluna para a soma total de hóspedes (adultos, crianças e bebês). Identifiquei e invalidei reservas com valores zero (0).
Métricas de receita (Business Intelligence): Criei uma nova coluna ‘df_revenue’ multiplicando ‘adr’ por ‘total_nights’. Considerei apenas reservas com data de check-out.

#Principais conclusões (insights)

Perfil do cliente: De acordo com os quartis (25%, 50%, 75%), o perfil predominante é o de casais (2 adultos) sem filhos.
Sazonalidade: A receita atinge seu pico em agosto, embora julho apresente uma alta densidade de pernoites.
Detecção de outliers: Identifiquei uma reserva atípica de um hóspede italiano (ITA) com um ADR de US$ 510, um valor muito superior à média de US$ 103,48, mesmo para uma categoria de quarto padrão (A).

#Visualização (Próximos passos)
Utilizei Seaborn e Matplotlib para representar:
Lineplot: Tendência de receita mensal (ordenada cronologicamente de janeiro a dezembro através de categorias).
Barplot: Ranking de receita por país de origem (Top 10) segmentado por tipo de hotel.

#Próximos Passos
Finalizar a integração dos dados limpos no Power BI para criação de dashboards dinâmicos.
