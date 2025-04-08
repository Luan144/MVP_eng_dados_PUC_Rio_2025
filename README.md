# MVP_eng_dados_PUC_Rio_2025

### Trabalho de conclusão da sprint Engenharia de Dados da especialização em Ciência de Dados e Analytics da Puc-Rio.

#### O objetivo deste trabalho é criar um pipeline de extração, limpeza e análise de dados.
 
#### Os dados utilizados nesse processo foram obtidos através do Portal da Transparência do Governo Federal e estão disponíveis no link https://portaldatransparencia.gov.br/emendas/visao-geral.

#### O Portal da Transparência conta com um glossário e um dicionário de dados, porém, por motivos práticos, segue abaixo o dicionário com apenas os dados utilizados na camada "Gold" do trabalho.

## Catálogo de dados:

#### codigo_emenda [str]: Identificador da emenda parlamentar, composto por 12 dígitos: 4 do ano da emenda + 4 do código do autor + 4 do número da emenda do autor.

#### ano_emenda [int]: Ano em que emenda foi proposta. Os valores vão de 2021 a 2024 de forma contínua.

#### tipo_emenda [str]: Descreve o tipo de emenda parlamentar. Sus categorias são: "Emenda Individual - Transferências com Finalidade Definida"; "Emenda Individual - Transferências Especiais"; "Emenda de Bancada"; "Emenda de Comissão"; "Emenda de Relator".

#### nome_autor [str]: Nome do autor da emenda parlamentar, conforme registrado no Sistema de Administração Financeira do Governo Federal - SIAFI.

#### local_destino [str]: Atributo do Plano de Trabalho que indica, durante a execução da despesa, a região onde a despesa ocorre. Os valores dessa categoria podem ser: nome do município em letras mísculas seguido da UF (exemplo: "COTIA - SP"); apenas nome do estado em letras maiúsculas seguido de "(UF)" (exemplo: "PARANÁ (UF)"); "Múltiplo" quando a emenda abrange diversas localidades; "Nacional" quando a emenda abrange todo o território nacional. 

#### municipio [str]: Nome do município de destinação do recurso. Os valores dessa categoria podem ser: nome do município em letras maiúsculas (exemplo: "JOÃO PESSOA"); "Múltiplo"; "Sem informação".

#### uf [str]: 	Nome do estado de destinação do recurso. Este campo poderá estar sem informação, a depender da localidade de aplicação. Os valores dessa categoria podem ser: nome da unidade federativa em letras maiúsculas (exemplo: "RIO DE JANEIRO")

#### regiao [str]: Região de destinação do recurso. Os valores dessa categoria podem ser: nome da região com primeira letra maiúscula (exemplo: "Nordeste"); "Múltiplo"; "Nacional"; "Exterior".

#### subfuncao [str]: Nome da subfunção em que foi classificada a despesa associada à emenda parlamentar. Os valores dessa categoria podem ser: nome da subfunção iniciando com letra maiúscula (exemplo: "Atenção básica").

#### valor_empenhado [float64]: Valor empenhado para a emenda. Reserva de valores monetários autorizados para atender um fim específico. Valores máximo e mínimo respectivamente (com casas decimais separadas por "."): 10,058,950,760.11 e 2,633.0.