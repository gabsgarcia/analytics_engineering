# analytics_engineering_project
Projeto: Engenharia de Dados e Garantia de Qualidade no Conjunto de Dados do Airbnb no Rio de Janeiro
Introdução à Base de Dados do Airbnb
O conjunto de dados "Inside Airbnb", disponível no website "http://insideairbnb.com/", é uma valiosa fonte de informações sobre listagens de hospedagem, avaliações de hóspedes e disponibilidade de calendário em várias cidades ao redor do mundo, incluindo o Rio de Janeiro. Antes de prosseguirmos com a engenharia de dados, é importante entender os principais componentes deste conjunto de dados:

Listing (Listagem): Este conjunto de dados contém informações detalhadas sobre as propriedades listadas no Airbnb. Cada registro representa uma listagem individual e inclui informações como o tipo de propriedade, preço, localização, número de quartos, comodidades oferecidas e muito mais.

Reviews (Avaliações): O conjunto de dados de avaliações contém informações sobre as avaliações feitas por hóspedes que ficaram nas propriedades listadas. Ele inclui dados como a data da avaliação, o identificador da propriedade, os comentários escritos pelos hóspedes, e outras informações.

Calendar (Calendário): Este conjunto de dados contém informações sobre a disponibilidade das propriedades ao longo do tempo. Ele lista as datas em que as propriedades estão disponíveis para reserva, bem como os preços para cada data.

O dicionário dos dados também está disponível no website: "http://insideairbnb.com/".

Passos do Projeto
Aquisição de Dados e Armazenamento de Dados em PostgreSQL - Camada Bronze
Baixe o conjunto de dados "Inside Airbnb" do Rio de Janeiro da fonte oficial (http://insideairbnb.com/) e promova uma estruturação simples nos dados.
Crie um banco de dados PostgreSQL para armazenar os dados brutos das 3 tabelas ("Listing", "Reviews" e Calendar") na camada "bronze".

Data Clean - Camada Silver:
Identifique e lide com valores ausentes, duplicatas e outliers nos dados brutos da camada "bronze".
Padronize e limpe os nomes das colunas, convertendo-os em um formato consistente.
Realize uma limpeza textual em campos, como descrições de propriedades, removendo caracteres especiais e erros de digitação.

Data Quality - Camada Silver:
Defina métricas de qualidade de dados, como integridade, precisão e consistência para os dados da camada "bronze".
Implemente verificações para garantir que os dados da camada "silver" estejam em conformidade com essas métricas.
Estabeleça um sistema de monitoramento contínuo da qualidade dos dados da camada "silver".

Testes de Qualidade - Camada Silver:
Utilize a biblioteca Great Expectations para criar testes de qualidade automatizados que verifiquem as expectativas definidas para os dados da camada "silver".
Desenvolva testes que assegurem que os dados da camada "silver" atendam às regras de negócios e aos requisitos de qualidade.

Transformação de Dados com dbt - Camada Silver:
Utilize a ferramenta dbt para criar a camada "silver" de dados, realizando transformações e preparando os dados da camada em questão.
Mantenha um controle de versão dos modelos dbt relacionados à camada "silver" e automatize a execução das transformações.

Armazenamento de Dados em PostgreSQL - Camada Silver:
Armazene os dados da camada "silver" no mesmo banco de dados PostgreSQL.
Estabeleça conexões entre o dbt e o PostgreSQL para carregar os dados transformados da camada "silver" no banco.

Validação de Expectativas com Great Expectations - Camada Silver:
Implemente validações adicionais usando Great Expectations nas camadas de dados da camada "silver".
Monitore a qualidade dos dados da camada "silver" após cada transformação e ajuste os testes de acordo.

Transformação de Dados com dbt - Camada Gold:
Utilize o dbt para criar a camada "gold" de dados, aplicando agregações especializadas, como médias de preços por propriedade, por período, e outras agregações especializadas.
Mantenha um controle de versão dos modelos dbt relacionados à camada "gold" e automatize a execução das transformações.
Armazene os dados da camada "gold" no mesmo banco de dados PostgreSQL, mantendo a estrutura de dados otimizada para consultas analíticas.

Apresentação e Discussão:
Apresente os resultados do projeto para a turma, enfatizando os aspectos de engenharia de dados, qualidade de dados e uso de ferramentas como dbt, Great Expectations e o armazenamento em um banco de dados PostgreSQL nas camadas "bronze", "silver" e "gold".
