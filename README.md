# Projeto de Controle de Velocidade com ESP32 e Node-RED

## Descrição do Projeto

Este projeto é o início de uma das partes do projeto do Formula E Hub. Ele visa simular a velocidade de um carro de Formula E utilizando um dispositivo IoT (ESP32) que se comunica via MQTT. Os dados de velocidade são enviados para um broker MQTT (HiveMQ) e, em seguida, visualizados através do Node-RED, permitindo uma representação gráfica em tempo real. Assim se tornando o início de um projeto que visa mostrar em tempo real a velocidade de cada carro em uma corrida em nosso site.

## Arquitetura Proposta

A arquitetura da solução envolve três principais componentes:

1. **Dispositivos IoT**:
   - **ESP32**: Responsável por medir e controlar a velocidade. Conectado a um botão para aumentar ou diminuir a velocidade e um display LCD para visualização local.

2. **Back-End**:
   - **Broker MQTT**: Utilizado para a troca de mensagens entre o ESP32 e o Node-RED.
   - **Node-RED**: Plataforma para a criação de fluxos que recebe os dados do MQTT e os apresenta em um dashboard por meio do gauge.

3. **Front-End**:
   - **Dashboard do Node-RED**: Interface gráfica para visualização em tempo real da velocidade, em que é utilizado o gauge.

## Recursos Necessários

### Dispositivos IoT
- **ESP32**
- **Display LCD I2C**
- **Botão Push Button**
- **Jumpers**
- **Resistores**

### Back-End
- **Broker MQTT** (HiveMQ)
- **Node-RED**

### Front-End
- **Node-RED Dashboard**

## Instruções de Uso

1. **Configuração do ESP32**:
   - Certifique-se de que o ESP32 esteja conectado à rede Wi-Fi e que o código fonte esteja carregado no dispositivo.
   - O código fonte deve ser modificado para incluir as credenciais de Wi-Fi e as configurações do broker MQTT, (no código do projeto foi utilizado "Wokwi-GUEST" que é uma rede Wi-Fi virtual que é disponibilizada pela plataforma de simulação Wokwi).

2. **Configuração do Node-RED**:
   - Instale e inicie o Node-RED.
   - Utilize os nodes MQTT para se conectar ao broker e receba as mensagens publicadas pelo ESP32.
   - Crie um dashboard para visualizar a velocidade em tempo real.

## Requisitos

- **Plataforma**: Arduino IDE
- **Bibliotecas**:
  - `WiFi.h`
  - `PubSubClient.h`
  - `LiquidCrystal_I2C.h`

## Dependências

- **Node-RED** deve estar instalado na máquina local ou em um servidor.
- Acesso à internet para conectar ao broker MQTT.

## Códigos Fonte

O código desenvolvido para o projeto está localizado no seguinte repositório: https://github.com/mm-dantas/Sprint3-Edge



## Membros do Grupo

- **Matheus Dantas** – RM: 558804
- **Marco Antonio Andrade Gonçalves** – RM: 556818
- **Silas Alves Santos** – RM: 555020
- **Camila Takara** – RM: 555418
