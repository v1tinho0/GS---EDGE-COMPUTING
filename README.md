# WorkBalance – Sistema de Pausas Inteligentes para Home Office

## Integrantes
- Victor Pereira -> RM:56158
- Vinicius Gama -> RM:561617
- Paulo Rodrigues -> RM:565998


## Descrição do Projeto
O WorkBalance é um sistema IoT desenvolvido com ESP32 que simula pausas inteligentes durante o home office. O objetivo é melhorar o bem-estar do profissional, equilibrando períodos de trabalho e descanso de forma automatizada, com notificações visuais via OLED e indicação de status por LED.

O projeto demonstra como a IoT e o conceito de automação podem contribuir para o **futuro do trabalho**, promovendo saúde, produtividade e integração tecnológica.

## Componentes Utilizados
- ESP32
- OLED 128x64 (I²C)
- LED indicador
- LDR (sensor de luminosidade)
- Resistores e conexões básicas

## Funcionamento
- **Trabalho**: 50 segundos simulando 50 minutos  
  - OLED mostra "Trabalhando 50 min"  
  - LED desligado  
  - Serial Monitor simula envio MQTT: `[SIMULAÇÃO MQTT] Tópico: YourWork/status | Mensagem: De volta ao trabalho`
- **Pausa**: 30 segundos simulando 30 minutos  
  - OLED mostra "Tempo de descanso 30 min"  
  - LED aceso  
  - Serial Monitor simula envio MQTT: `[SIMULAÇÃO MQTT] Tópico: YourWork/status | Mensagem: Hora da pausa!`
- Contagem regressiva visível no OLED em segundos  
- Ciclo automático repetitivo

## Link da Simulação Wokwi
[Visualizar projeto no Wokwi](https://wokwi.com/projects/447465378467208193)

## Explicação Técnica – MQTT Simulado
O projeto utiliza o **Serial Monitor** para simular mensagens MQTT, mostrando quais tópicos e mensagens seriam enviados a um broker real em um ESP32 físico.  
- Tópico: `YourWork/status`  
- Mensagens: `"Hora da pausa!"` e `"De volta ao trabalho"`  
- Prefixo `[SIMULAÇÃO MQTT]` para indicar que é simulado  
- Essa abordagem permite demonstrar a funcionalidade do sistema mesmo sem conexão Wi-Fi real no Wokwi.

## Instruções de Uso
1. Abra o projeto no [Wokwi](https://wokwi.com/projects/447465378467208193).  
2. Inicie a simulação.  
3. Observe:  
   - OLED exibindo status e contagem regressiva  
   - LED indicando pausa  
   - Serial Monitor mostrando mensagens MQTT simuladas  

## Benefícios e Impacto
- Promove pausas automáticas e monitoramento do tempo de trabalho  
- Facilita a organização pessoal e melhora a produtividade  
- Demonstra como a IoT pode ser integrada ao **futuro do trabalho**  

