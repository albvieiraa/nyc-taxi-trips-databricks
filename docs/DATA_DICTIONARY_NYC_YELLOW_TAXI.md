# NYC Yellow Taxi Trip Data — Dicionário de Dados

## Contexto

A Taxi & Limousine Commission (TLC) da cidade de Nova York mantém dados de todas as viagens realizadas por seus veículos regulamentados. Esses dados são públicos e podem ser baixados diretamente do site oficial da TLC.

A TLC gerencia dados de quatro tipos principais de veículos:

- **Yellow Taxi (Táxi Amarelo)**  
  São os tradicionais táxis amarelos de Nova York, que operam exclusivamente por meio de corridas solicitadas na rua (street hails). O número de táxis é limitado por um sistema de medallions emitidos pela TLC. As corridas não são pré-agendadas.

- **Green Taxi (Street Hail Livery)**  
  Veículos identificados pela cor verde, autorizados a aceitar corridas na rua em regiões fora de Manhattan, além de corridas pré-agendadas.

- **For-Hire Vehicles (FHV)**  
  Veículos acessados apenas por meio de agendamento prévio com empresas ou aplicativos. Não podem aceitar corridas na rua.

## Escopo deste Projeto

Neste projeto, são considerados **apenas dados de Yellow Taxis**, referentes aos seguintes períodos:
- Janeiro de 2015
- Janeiro a Março de 2016

Os arquivos utilizados fazem parte de uma versão anterior do dataset da TLC, na qual ainda são fornecidas as **coordenadas geográficas (latitude e longitude)** de pickup e dropoff.

Versões mais recentes do dataset substituem as coordenadas por **identificadores de zonas**, devido a mudanças na forma de disponibilização dos dados pela TLC.

## Dicionário de Campos

| Nome da Coluna | Descrição |
|---------------|-----------|
| **VendorID** | Código que identifica o provedor do sistema TPEP que registrou a viagem. <br>Valores comuns: <br>• 1 = Creative Mobile Technologies <br>• 2 = VeriFone Inc. |
| **tpep_pickup_datetime** | Data e hora em que o taxímetro foi acionado (início da corrida). |
| **tpep_dropoff_datetime** | Data e hora em que o taxímetro foi desligado (fim da corrida). |
| **passenger_count** | Número de passageiros no veículo. Valor informado manualmente pelo motorista. |
| **trip_distance** | Distância total da viagem em milhas, registrada pelo taxímetro. |
| **pickup_longitude** | Longitude do local onde a corrida foi iniciada. |
| **pickup_latitude** | Latitude do local onde a corrida foi iniciada. |
| **RateCodeID** | Código da tarifa aplicada ao final da corrida. <br>Valores possíveis: <br>• 1 = Tarifa padrão <br>• 2 = JFK <br>• 3 = Newark <br>• 4 = Nassau ou Westchester <br>• 5 = Tarifa negociada <br>• 6 = Viagem em grupo |
| **store_and_fwd_flag** | Indica se o registro da viagem foi armazenado temporariamente no veículo antes de ser enviado ao sistema (store and forward), devido à falta de conexão. <br>• Y = Sim <br>• N = Não |
| **dropoff_longitude** | Longitude do local onde a corrida foi finalizada. |
| **dropoff_latitude** | Latitude do local onde a corrida foi finalizada. |
| **payment_type** | Código numérico que indica a forma de pagamento. <br>Valores possíveis: <br>• 1 = Cartão de crédito <br>• 2 = Dinheiro <br>• 3 = Sem cobrança <br>• 4 = Contestação <br>• 5 = Desconhecido <br>• 6 = Viagem cancelada |
| **fare_amount** | Valor da tarifa calculada pelo taxímetro, com base em tempo e distância. |
| **extra** | Encargos adicionais e sobretaxas, como taxas de horário de pico ou período noturno. |
| **mta_tax** | Taxa fixa da MTA (Metropolitan Transportation Authority), no valor de $0.50, aplicada automaticamente conforme a tarifa. |
| **improvement_surcharge** | Taxa de melhoria no valor de $0.30, aplicada no início da corrida. Introduzida em 2015. |
| **tip_amount** | Valor da gorjeta. Preenchido automaticamente apenas para pagamentos com cartão de crédito. Gorjetas em dinheiro não são incluídas. |
| **tolls_amount** | Valor total de pedágios pagos durante a viagem. |
| **total_amount** | Valor total cobrado do passageiro, excluindo gorjetas em dinheiro. |


## Observações de Qualidade dos Dados

- `passenger_count` pode conter valores inválidos
- coordenadas podem estar zeradas
- gorjetas só aparecem em cartão

