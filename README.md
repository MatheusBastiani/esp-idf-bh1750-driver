# ESP-IDF CLion Template 🚀

This repository is a C++ boilerplate template for embedded systems development using the ESP32 microcontroller family and the ESP-IDF framework. The environment comes pre-configured for the JetBrains CLion IDE with built-in support for FreeRTOS tasks.

## 🛠️ Technologies
*   **Microcontroller:** ESP32 Family
*   **Framework:** ESP-IDF v5.x
*   **Language:** C++
*   **RTOS:** FreeRTOS
*   **Build System:** CMake + Ninja
*   **IDE:** JetBrains CLion

## 📋 Prerequisites
Before cloning this template, ensure you have the following installed and configured on your system:
1.  [ESP-IDF](https://docs.espressif.com/projects/esp-idf/en/latest/esp32/get-started/index.html) successfully installed.
2.  JetBrains CLion IDE.
3.  The official "Espressif ESP-IDF" plugin installed within CLion.

## ⚙️ How to Use This Template
1.  Click the green **"Use this template"** button on GitHub to generate your new repository.
2.  Clone your newly created repository to your local machine.
3.  Open the cloned folder in CLion.
4.  Navigate to `File > Settings > Build, Execution, Deployment > CMake`.
5.  Under the **Environment** section, add the necessary environment variables for your system:
    *   `IDF_PATH`: The installation path of your ESP-IDF (e.g., `C:\esp\v6.0\esp-idf`).
    *   `PYTHON`: The path to the Python executable inside the Espressif virtual environment.
6.  Under **Toolchains**, ensure the `export.bat` (or `export.sh` for Linux/macOS) is set in the *Environment script* field.
7.  Click **Reload CMake Project**.

## 📁 Project Structure
The main application logic and FreeRTOS tasks should be implemented in the core source file:
`main/main.cpp`
