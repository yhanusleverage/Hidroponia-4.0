 # 🌱 Sistema de Controle Hidropônico IoT

## Descrição
Este é um sistema inteligente de controle hidropônico que monitora e controla parâmetros essenciais para o cultivo de plantas em hidroponia. O sistema utiliza um ESP32 como controlador principal, conectado a diversos sensores e relés para automação completa.

## 📊 Parâmetros Monitorados
- **Temperatura da Água**: 18-24°C (ideal)
- **pH**: 5,5-6,5 (ideal para maioria das plantas)
- **EC (Electrical Conductivity)**: 0,8-2,4 mS/cm (varia conforme cultura)
- **TDS (Total Dissolved Solids)**: 400-1.200 ppm (varia conforme cultura)

## 🎛️ Controles Automatizados
O sistema controla 8 relés para diferentes funções:
1. Bomba pH- (redução de pH)
2. Bomba pH+ (aumento de pH)
3. Bomba A (nutrientes)
4. Bomba B (nutrientes)
5. Bomba C (nutrientes)
6. Bomba Principal
7. Luz UV
8. Aerador

## 💻 Interface Web
- Interface amigável e responsiva
- Gráficos em tempo real
- Controle manual dos relés
- Temporizadores para dosagem precisa
- Monitoramento remoto via ThingSpeak

## 🔧 Componentes Principais
- ESP32 (controlador principal)
- Sensores:
  - DS18B20 (temperatura)
  - Sensor de pH
  - Sensor EC/TDS
- Display LCD I2C
- 2x PCF8574 (expansores I2C para relés)
- 8 Relés para controle

## 📁 Estrutura do Projeto

### `/include` (Arquivos de Cabeçalho)
- `HydroControl.h`: Classe principal do sistema
- `PHSensor.h`: Controle do sensor de pH
- `TDSReaderSerial.h`: Controle do sensor EC/TDS
- `WebServerManager.h`: Gerenciamento do servidor web
- `ThingSpeakManager.h`: Integração com ThingSpeak

### `/src` (Código Fonte)
- `main.cpp`: Arquivo principal
- `HydroControl.cpp`: Implementação do controle
- `PHSensor.cpp`: Implementação do sensor pH
- `TDSReaderSerial.cpp`: Implementação EC/TDS
- `WebServerManager.cpp`: Servidor web
- `ThingSpeakManager.cpp`: Comunicação ThingSpeak

### `/data` (Interface Web)
- `index.html`: Página principal
- `style.css`: Estilos da interface
- `script.js`: Funcionalidades JavaScript

## 🚀 Funcionalidades Principais

### Monitoramento Automático
- Leitura contínua de todos os sensores
- Atualização em tempo real no display LCD
- Envio de dados para nuvem (ThingSpeak)

### Controle de Dosagem
- Bombas peristálticas com temporizador
- Dosagem precisa de nutrientes
- Controle automático de pH

### Interface Web
- Gráficos de tendência
- Controles manuais
- Status em tempo real
- Design responsivo

## ⚙️ Parâmetros Ideais para Hidroponia

### Temperatura
- **Ideal**: 18-24°C
- **Motivo**: Afeta absorção de nutrientes e oxigênio

### pH
- **Ideal**: 5,5-6,5
- **Motivo**: Crucial para absorção de nutrientes

### EC/TDS
- **Vegetais Folhosos**: 0,8-1,2 mS/cm (400-600 ppm)
- **Tomates/Pimentões**: 2,0-2,4 mS/cm (1000-1200 ppm)
- **Motivo**: Indica concentração de nutrientes

## 📈 Monitoramento Remoto
- Dados enviados para ThingSpeak a cada 15 segundos
- Gráficos históricos disponíveis
- Acesso remoto via navegador

## 🔍 Manutenção
- Calibração mensal dos sensores de pH
- Limpeza semanal do sensor EC/TDS
- Verificação mensal das bombas peristálticas
- Troca da solução nutritiva a cada 2-3 semanas

## ⚠️ Alertas
O sistema monitora:
- Níveis críticos de pH
- Temperatura fora da faixa ideal
- EC/TDS muito alto/baixo
- Falhas nas bombas

## 🌟 Benefícios
- Automação completa
- Economia de água e nutrientes
- Monitoramento preciso
- Controle remoto
- Histórico de dados
- Interface amigável

---
Desenvolvido com ❤️ para hidroponia brasileira
