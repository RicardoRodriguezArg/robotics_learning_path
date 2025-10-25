# 🤖 Learning Path Full Stack Robotics  
**Duración total:** 18 meses (6 trimestres)  
**Lenguaje principal:** C++20  
**Enfoques integrados:** Embebidos • Robótica • Computer Vision • Machine Learning • OpenCL • IA • UI

---

## 🧠 ETAPA 1 — Concepts, Ejercicios y Tests  
> Objetivo: dominar los fundamentos teóricos y prácticos en C++20, control, robótica, visión y ML embebido.

---

### 🔹 Nivel Básico

#### 💡 Conceptos Clave
- C++20 moderno: RAII, templates, coroutines, multithreading  
- Control clásico: PID, filtros digitales  
- Estructuras de datos y algoritmos fundamentales  
- Comunicación MCU ↔ PC: UART, SPI, I2C  
- Introducción a visión (OpenCV básico) y TinyML  
- Optimización de memoria en sistemas embebidos  

#### 🧩 Ejercicios y Tests
- Implementar estructuras de datos en C++20  
- Control PID y filtros digitales en MCU  
- Comunicación UART + GUI C++ (ImGui)  
- Reimplementar código (C / Go / Rust → C++20)  
- Test de complejidad, modularidad y eficiencia  

---

### 🔹 Nivel Avanzado

#### 💡 Conceptos Clave
- Algoritmos de planificación (A*, D*, RRT*)  
- Filtros de Kalman y LQR  
- Concurrencia avanzada: threads, futures, coroutines  
- Paralelismo con OpenCL  
- Protocolos embebidos (CAN, RS-485)  
- CNNs pequeñas y ML clásico en C++20  

#### 🧩 Ejercicios y Tests
- Portar controladores de C a C++20/OpenCL  
- Planificador A* con visualización  
- Pipeline de visión paralelizado (OpenCL)  
- Driver CAN básico + comunicación bidireccional  
- Tests de optimización de memoria y rendimiento  

---

### 🔹 Nivel Challenge

#### 💡 Conceptos Clave
- SLAM visual y mapeo 3D  
- Aprendizaje por refuerzo aplicado al control  
- Implementar redes neuronales desde cero (C++20)  
- Fusión sensorial avanzada (IMU + LIDAR + visión)  
- Arquitectura modular y benchmarking embebido  

#### 🧩 Ejercicios y Tests
- Filtro de Kalman extendido (EKF completo)  
- CNN manual + OpenCL  
- Pipeline de inferencia optimizado  
- Integración de sensores múltiples  
- Test: estabilidad y determinismo bajo RTOS  

---

## ⚙️ ETAPA 2 — Ejercicios Integradores  
> Objetivo: aplicar los conocimientos adquiridos en proyectos reales y multidisciplinares.

---

### 🔹 Nivel Básico — Proyectos de Integración Simple

| Proyecto | Descripción | Foco Técnico | RTOS |
|-----------|--------------|--------------|------|
| **Mini Gimbal 1 Eje** | Control IMU + servo + GUI | PID, sensores, FreeRTOS | FreeRTOS |
| **Brazo Robótico 3DOF** | Control desde GUI C++ | Cinemática directa | Zephyr |
| **Robot Seguidor de Línea** | Control diferencial con IR | Control PID y sensores | FreeRTOS |
| **Clasificador de Color** | Cámara + cinta transportadora | OpenCV básico + GPIO | Mbed |
| **Monitor de Sensores** | GUI C++ con telemetría | Threads, buffers circulares | Zephyr |

---

### 🔹 Nivel Avanzado — Sistemas Autónomos Medianos

| Proyecto | Descripción | Foco Técnico | RTOS / SO |
|-----------|--------------|--------------|------------|
| **Plataforma Giroestabilizada 3 Ejes** | Control multivariable + GUI | OpenCL + control avanzado | NuttX |
| **Robot Logístico Autónomo (Warehouse Mini)** | SLAM 2D + planificación | ROS2 + planificación | ROS2 + PREEMPT-RT |
| **Brazo Pick & Place con Visión** | Detección + cinemática inversa | CNN simple, OpenCL | NuttX |
| **Dashboard Robótico Multisensorial** | UI Qt con video + datos | Concurrencia, sockets | Linux RT |
| **Vehículo Autónomo a Escala** | ML embebido para conducción | TinyML + visión | PREEMPT-RT |

---

### 🔹 Nivel Challenge — Investigación y Robótica Inteligente

| Proyecto | Descripción | Foco Técnico | RTOS / SO |
|-----------|--------------|--------------|------------|
| **Sistema Multi-Robot Cooperativo** | Coordinación distribuida DDS | ROS2 + micro-ROS | ROS2 |
| **Brazo Colaborativo con RL** | Aprendizaje por refuerzo | Q-learning, sim-to-real | Xenomai |
| **Plataforma Giroestabilizada con IA Predictiva** | Predicción con RNN/LSTM | IA + control predictivo | PREEMPT-RT |
| **Sistema de Inspección 3D Inteligente** | Visión 3D + defect detection | OpenCL 3D + ML | ROS2 |
| **Digital Twin Robótico Completo** | Simulación real conectada | ROS2 + sincronización RT | Yocto RT |
| **Sistema Autónomo de Navegación Visual** | SLAM + RL adaptativo | Aprendizaje continuo | ROS2 / Xenomai |

---

## 🧩 RTOS y SO por Nivel de Complejidad

| Nivel | RTOS / SO | Hardware Sugerido | Aplicación |
|--------|-------------|------------------|-------------|
| **Básico** | FreeRTOS, Zephyr, Mbed, RIOT | STM32, ESP32, RP2040 | Controladores, sensores |
| **Avanzado** | NuttX, ChibiOS, QNX, ThreadX | STM32H7, Teensy 4.x, Jetson Nano | Robótica + multitarea |
| **Challenge** | PREEMPT-RT, Xenomai, ROS2/micro-ROS, Yocto RT | Raspberry Pi 5, Jetson Xavier, BeagleBone AI | Robótica distribuida + IA embebida |

---

## 🗓️ ROADMAP TRIMESTRAL (Formato Gantt)

### 🕐 **Trimestre 1 — Fundamentos C++20 + Control**
| Semana | Tema | Entregable | RTOS |
|--------|------|-------------|------|
| 1–4 | Sintaxis y estructuras C++20 | Ejercicios RAII y estructuras | — |
| 5–8 | Control PID + sensores | PID funcional en simulación | FreeRTOS |
| 9–12 | Comunicación MCU ↔ PC | Telemetría GUI | Zephyr |

✅ **Meta:** dominio base de control y comunicación en C++20.

---

### 🕑 **Trimestre 2 — Algoritmos + ML Básico**
| Semana | Tema | Entregable | RTOS |
|--------|------|-------------|------|
| 1–4 | A*, Kalman, LQR | Simulador de navegación | NuttX |
| 5–8 | Paralelismo + OpenCL | Pipeline paralelo de visión | Zephyr |
| 9–12 | TinyML e inferencia | Clasificador ML simple | ChibiOS |

✅ **Meta:** dominio de algoritmos embebidos y optimización básica.

---

### 🕒 **Trimestre 3 — Visión por Computador + GPU**
| Semana | Tema | Entregable | RTOS |
|--------|------|-------------|------|
| 1–4 | OpenCV + CNN | Detección de color y formas | PREEMPT-RT |
| 5–8 | OpenCL kernels | Aceleración de convoluciones | PREEMPT-RT |
| 9–12 | Integración con hardware | Robot con cámara + GUI | NuttX |

✅ **Meta:** visión acelerada en hardware embebido.

---

### 🕓 **Trimestre 4 — Proyectos Integradores Iniciales**
| Proyecto | Enfoque | RTOS |
|-----------|----------|------|
| Mini Gimbal 1 Eje | Control + IMU + GUI | FreeRTOS |
| Brazo 3DOF | Cinemática directa + GUI Qt | Zephyr |
| Robot Seguidor de Línea | Control diferencial | Mbed |

✅ **Meta:** sistemas simples completamente integrados.

---

### 🕔 **Trimestre 5 — Proyectos Avanzados**
| Proyecto | Enfoque | RTOS / SO |
|-----------|----------|------------|
| Plataforma Giroestabilizada | Control multivariable | NuttX |
| Robot Warehouse | SLAM + planificación | ROS2 + RT |
| Pick & Place | Visión + cinemática inversa | NuttX |
| Dashboard | Visualización avanzada | Linux RT |

✅ **Meta:** integración completa de control + visión + ML.

---

### 🕕 **Trimestre 6 — Challenge e Investigación**
| Proyecto | Enfoque | RTOS / SO |
|-----------|----------|------------|
| Multi-Robot Cooperativo | ROS2 + DDS distribuido | ROS2 |
| Brazo Colaborativo RL | Aprendizaje por refuerzo | Xenomai |
| IA Predictiva / Digital Twin | Modelos LSTM + simulación RT | ROS2 / Yocto RT |

✅ **Meta:** robótica autónoma con IA embebida y coordinación distribuida.

---

## 📈 VISIÓN GANTT GLOBAL

```text
T1 |████████████| Fundamentos C++20 + Control (FreeRTOS)
T2 |████████████| Algoritmos + ML básico (NuttX)
T3 |████████████| OpenCL + Visión por Computador (PREEMPT-RT)
T4 |████████████| Proyectos Iniciales (Mini Gimbal, Brazo, Robot)
T5 |████████████| Proyectos Avanzados (Giroestabilizado, Warehouse Bot)
T6 |████████████| Challenge: Multi-Robot + IA Predictiva + Digital Twin

