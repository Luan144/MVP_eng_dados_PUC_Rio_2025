# MVP_eng_dados_PUC_Rio_2025

### Trabalho de conclusão da sprint Engenharia de Dados da especialização em Ciência de Dados e Analytics da Puc-Rio.

#### O objetivo deste trabalho é criar um pipeline de extração, limpeza e análise de dados.
 
#### Os dados utilizados nesse processo foram obtidos através do Portal da Transparência do Governo Federal e estão disponíveis no link https://portaldatransparencia.gov.br/emendas/visao-geral.

#### O Portal da Transparência conta com um glossário e um dicionário de dados, porém, por motivos práticos, segue abaixo o dicionário com apenas os dados utilizados na camada "Gold" do trabalho.

## Catálogo de dados:

### Campos da Tabela de Emendas Parlamentares

- **`codigo_emenda` [str]**  
  Identificador da emenda parlamentar, composto por 12 dígitos:  
  - 4 do ano da emenda  
  - 4 do código do autor  
  - 4 do número da emenda do autor

- **`ano_emenda` [int]**  
  Ano em que a emenda foi proposta.  
  Valores possíveis: **2021 a 2024** (de forma contínua)

- **`tipo_emenda` [str]**  
  Descreve o tipo de emenda parlamentar. As categorias são:  
  - *Emenda Individual - Transferências com Finalidade Definida*  
  - *Emenda Individual - Transferências Especiais*  
  - *Emenda de Bancada*  
  - *Emenda de Comissão*  
  - *Emenda de Relator*

- **`nome_autor` [str]**  
  Nome do autor da emenda parlamentar, conforme registrado no SIAFI (Sistema de Administração Financeira do Governo Federal).

- **`local_destino` [str]**  
  Indica a região onde a despesa ocorre, segundo o Plano de Trabalho.  
  Exemplos de valores:  
  - `"cotia - SP"`  
  - `"PARANÁ (UF)"`  
  - `"Múltiplo"`  
  - `"Nacional"`

- **`municipio` [str]**  
  Nome do município de destinação do recurso.  
  Exemplos de valores:  
  - `"JOÃO PESSOA"`  
  - `"Múltiplo"`  
  - `"Sem informação"`

- **`uf` [str]**  
  Nome do estado de destinação do recurso.  
  Pode estar em branco em alguns casos.  
  Exemplos de valores:  
  - `"RIO DE JANEIRO"`  
  - *em branco*

- **`regiao` [str]**  
  Região de destinação do recurso.  
  Exemplos de valores:  
  - `"Nordeste"`  
  - `"Múltiplo"`  
  - `"Nacional"`  
  - `"Exterior"`

- **`subfuncao` [str]**  
  Nome da subfunção orçamentária associada à emenda parlamentar.  
  Exemplo de valor: `"Atenção básica"`

- **`valor_empenhado` [float64]**  
  Valor empenhado (reserva de recursos autorizada para uma despesa específica).  
  Valores possíveis (em reais):  
  - Mínimo: `2,633.0`  
  - Máximo: `10,058,950,760.11`
