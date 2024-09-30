# Projeto de Controle de Velocidade com ESP32 e Node-RED

## Descrição do Projeto

Este projeto visa desenvolver uma solução de controle de velocidade utilizando um dispositivo IoT (ESP32) que se comunica via MQTT. Os dados de velocidade são enviados para um broker MQTT (HiveMQ) e, em seguida, visualizados através do Node-RED, permitindo uma representação gráfica em tempo real.

## Arquitetura Proposta

A arquitetura da solução envolve três principais componentes:

1. **Dispositivos IoT**:
   - **ESP32**: Responsável por medir e controlar a velocidade. Conectado a um botão para aumentar ou diminuir a velocidade e um display LCD para visualização.

2. **Back-End**:
   - **Broker MQTT**: Utilizado para a troca de mensagens entre o ESP32 e o Node-RED.
   - **Node-RED**: Plataforma para a criação de fluxos que recebe os dados do MQTT e os apresenta em um dashboard.

3. **Front-End**:
   - **Dashboard do Node-RED**: Interface gráfica para visualização em tempo real da velocidade.

## Recursos Necessários

### Dispositivos IoT
- **ESP32**
- **Display LCD I2C**
- **Botão Push Button**

### Back-End
- **Broker MQTT** (HiveMQ)
- **Node-RED**

### Front-End
- **Node-RED Dashboard**

## Instruções de Uso

1. **Configuração do ESP32**:
   - Certifique-se de que o ESP32 esteja conectado à rede Wi-Fi e que o código fonte esteja carregado no dispositivo.
   - O código fonte deve ser modificado para incluir as credenciais de Wi-Fi e as configurações do broker MQTT.

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

Os códigos desenvolvidos para o projeto estão localizados na pasta `src/`. O arquivo principal `main.ino` contém a lógica de controle de velocidade.
