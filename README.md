🏨 Análise Exploratória de Dados: Reservas de Hotel (Hotel Bookings)

Este projeto consiste em uma Análise Exploratória de Dados (EDA) realizada sobre um conjunto de dados de reservas de hotéis (hotel_bookings.csv). Utilizando Python e a biblioteca Pandas, o objetivo é inspecionar a qualidade dos dados, identificar padrões de comportamento dos hóspedes e detectar possíveis anomalias no registro de diárias e reservas.

📊 Visão Geral do Dataset

O conjunto de dados reúne registros de reservas de hotéis, contendo 119.390 linhas e 32 colunas. Entre as principais variáveis analisadas estão:

Identificação e Datas: Tipo de hotel, datas de chegada (ano, mês, dia e número da semana) e tempo de antecedência da reserva (lead_time).

Hóspedes: Número de adultos, crianças, bebês, país de origem (country) e histórico de hóspede recorrente (is_repeated_guest).

Financeiro e Reservas: Preço médio da diária (adr), status de cancelamento (is_canceled), solicitações especiais e canais/agências de reserva (agent, company).

🔍 Principais Análises Realizadas

Inspeção Estrutural e Tipagem:

Verificação das dimensões (shape), visualização inicial das primeiras linhas (head) e identificação dos tipos de dados (dtypes, info).

Contagem de cardinalidade dos atributos (nunique).

Qualidade dos Dados e Valores Nulos:

Quantificação de campos nulos em valores absolutos e percentuais.

Constatação de alto índice de valores ausentes em colunas como company (~94,3%) e agent (~13,7%), além de pequenos percentuais em country e children.

Estatísticas Descritivas e Detecção de Inconsistências:

Aplicação de describe() para avaliação de médias, desvios e limites (mínimos e máximos).

Detecção de uma reserva com valor negativo no campo de diária (adr = -6.38), sinalizando um caso pontual a ser tratado ou investigado.

Observação de valores extremos de antecedência (lead_time máximo de 737 dias) e grupos com alto número de adultos (até 55 adultos em um único registro).

Agrupamentos e Comportamento por País:

Cálculo das médias de variáveis numéricas agrupadas por país (country).

Identificação dos países com maior fluxo de hóspedes: destaque para Portugal (PRT), Reino Unido (GBR), França (FRA), Espanha (ESP) e Alemanha (DEU).

Proporção percentual das origens dos hóspedes.

Intermediação de Reservas:

Análise de frequência de reservas por código de agência (agent) e corporação (company).

🛠️ Tecnologias Utilizadas

Python 3

Pandas (Leitura, manipulação, agregação e limpeza de dados)

Jupyter Notebook
