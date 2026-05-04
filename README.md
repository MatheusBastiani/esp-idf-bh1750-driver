# ESP32 BH1750 Light Sensor Reader ☀️

> 🚧 **Status do Projeto:** Em desenvolvimento inicial.

Este projeto tem como objetivo realizar a leitura de dados de luminosidade ambiente (em Lux) utilizando o sensor I2C **BH1750** e um microcontrolador **ESP32**. 

O firmware está sendo desenvolvido inteiramente em **C++** utilizando o framework **ESP-IDF**, aproveitando recursos de orientação a objetos e o **FreeRTOS** para o gerenciamento da tarefa de leitura contínua.

## 🧰 Stack Tecnológico
*   **Placa:** ESP32 (Qualquer variante genérica)
*   **Sensor:** Módulo BH1750FVI (I2C)
*   **Framework:** ESP-IDF v5.x
*   **Linguagem:** C++17
*   **Ambiente:** JetBrains CLion (gerado via template padrão)

## 🔌 Conexões de Hardware (Pinout)
A comunicação com o BH1750 é feita via protocolo I2C. Abaixo está a tabela de conexões padrão recomendada para o ESP32:

| Pino no BH1750 | Pino no ESP32 | Função |
| :--- | :--- | :--- |
| **VCC** | 3V3 | Alimentação (3.3V) |
| **GND** | GND | Terra |
| **SCL** | GPIO 22 | Clock do I2C |
| **SDA** | GPIO 21 | Dados do I2C |
| **ADD** | GND ou Não conectado | Define o endereço I2C (GND = `0x23`) |

*Nota: O pino ADD conectado ao GND (ou flutuando na maioria dos módulos) define o endereço do sensor como `0x23`. Se conectado em 3.3V, o endereço muda para `0x5C`.*

## 🚀 Como Executar
Este projeto foi construído usando uma base pré-configurada para o CLion.
1. Clone o repositório.
2. Abra no CLion e certifique-se de que as variáveis de ambiente `IDF_PATH` e o `PYTHON` do ESP-IDF estão configurados na aba de opções do CMake.
3. Configure o *Toolchain script* apontando para o seu `export.bat`.
4. Faça o *Reload* do CMake e compile.

## 📝 Roadmap de Desenvolvimento (To-Do)
- [x] Inicializar repositório a partir do template CLion + ESP-IDF.
- [ ] Criar a estrutura da classe C++ (ex: `BH1750.h` e `BH1750.cpp`).
- [ ] Configurar os parâmetros do barramento I2C (`i2c_param_config` e `i2c_driver_install`).
- [ ] Enviar comando de *Power On* e *Configuração de Resolução* para o sensor.
- [ ] Criar uma task no FreeRTOS (`xTaskCreate`) para ler e imprimir os valores em Lux no terminal periodicamente.
