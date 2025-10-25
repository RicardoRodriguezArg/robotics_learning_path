# 🧠 ETAPA 1 — NIVEL BÁSICO  
### 💡 Conceptos Clave  
C++20 moderno · Control clásico · Comunicación embebida · Visión básica · TinyML · Optimización de memoria

---

## 🗓️ Duración total: 12 semanas (1 trimestre)
**Carga sugerida:** 8–10 h/semana → ~100 h totales  
**Estructura:** 3 bloques de 4 semanas cada uno  

---

## 🧩 BLOQUE 1 — Fundamentos de C++20 Moderno (Semanas 1–4)

| Ejercicio | Objetivo | Duración estimada | Tests requeridos | RTOS / SO |
|------------|-----------|-------------------|------------------|-----------|
|------------|-----------|-------------------|------------------|-----------|
| **E1.1 — RAII aplicado a control de recursos embebidos** | Implementar clases RAII para manejar buffers, timers y periféricos MCU. | 6 h | 🧪 **Seguridad:** evitar fugas de memoria y acceso a recursos no liberados. | **FreeRTOS** |
|------------|-----------|-------------------|------------------|-----------|
| **E1.2 — Templates para controladores genéricos** | Crear una clase template `Controller<T>` que permita cambiar el tipo de sensor o actuador. | 6 h | 🧪 **Eficiencia:** evaluar tiempo de compilación y tamaño binario. | **Zephyr RTOS** |
|------------|-----------|-------------------|------------------|-----------|
| **E1.3 — Coroutines para tareas periódicas** | Implementar una coroutine que ejecute un bucle de lectura de sensor cada X ms. | 8 h | 🧪 **Performance:** latencia media < 10 ms. | **Zephyr RTOS** |
|------------|-----------|-------------------|------------------|-----------|
| **E1.4 — Multithreading con `std::thread` y `mutex`** | Simular dos tareas concurrentes (sensado y registro). | 8 h | 🧪 **Seguridad:** verificar ausencia de race conditions y deadlocks. | **Linux (PC)** |
|------------|-----------|-------------------|------------------|-----------|

**🧾 Sub-entregable:**  
**Task Manager C++20** — scheduler ligero con RAII + threads + coroutines.

---

## 🧩 BLOQUE 2 — Control Clásico y Señales (Semanas 5–8)

| Ejercicio | Objetivo | Duración estimada | Tests requeridos | RTOS / SO |
|------------|-----------|-------------------|------------------|-----------|
|------------|-----------|-------------------|------------------|-----------|
| **E2.1 — Implementación de PID en C++20** | Implementar clase `PIDController` parametrizable (Kp, Ki, Kd). | 6 h | 🧪 **Performance:** overshoot < 10 %. | **FreeRTOS** |
|------------|-----------|-------------------|------------------|-----------|
| **E2.2 — Filtro digital de media móvil y Butterworth** | Implementar y comparar filtros paso bajo. | 6 h | 🧪 **Eficiencia:** uso de CPU < 5 % en MCU. | **Mbed OS** |
|------------|-----------|-------------------|------------------|-----------|
| **E2.3 — Simulador de control en PC** | Controlar una masa-resorte-amortiguador con PID. | 8 h | 🧪 **Seguridad:** evitar overflow y saturación numérica. | **Linux (PC)** |
|------------|-----------|-------------------|------------------|-----------|
| **E2.4 — Control de motor DC con FreeRTOS** | Ejecutar el lazo PID en tiempo real (MCU o simulador). | 10 h | 🧪 **Performance:** jitter < 2 ms · **Eficiencia:** CPU < 50 %. | **FreeRTOS / Zephyr** |
|------------|-----------|-------------------|------------------|-----------|

**🧾 Sub-entregable:**  
**PID Engine** — biblioteca C++20 para control clásico en MCU + simulación PC.

---

## 🧩 BLOQUE 3 — Comunicación · Visión · TinyML (Semanas 9–12)

| Ejercicio | Objetivo | Duración estimada | Tests requeridos | RTOS / SO |
|------------|-----------|-------------------|------------------|-----------|
|------------|-----------|-------------------|------------------|-----------|
| **E3.1 — Comunicación UART y SPI con C++20** | Implementar drivers ligeros para UART y SPI (envío de datos de sensor). | 6 h | 🧪 **Seguridad:** CRC verificado · sin pérdida de paquetes. | **Zephyr RTOS** |
|------------|-----------|-------------------|------------------|-----------|
| **E3.2 — GUI de telemetría básica (ImGui o Qt)** | Mostrar datos recibidos desde MCU en tiempo real. | 8 h | 🧪 **Performance:** latencia visual < 100 ms. | **Linux (PC)** |
|------------|-----------|-------------------|------------------|-----------|
| **E3.3 — Detección de color con OpenCV** | Capturar imagen, segmentar color primario y calcular centroides. | 6 h | 🧪 **Eficiencia:** FPS ≥ 10 · CPU ≤ 70 %. | **Linux / PREEMPT-RT** |
|------------|-----------|-------------------|------------------|-----------|
| **E3.4 — TinyML: modelo de regresión lineal embebido** | Entrenar modelo simple (Python) y ejecutar inferencia en C++20. | 8 h | 🧪 **Performance:** inferencia < 1 ms · **Seguridad:** sin overflow. | **Mbed OS / FreeRTOS** |
|------------|-----------|-------------------|------------------|-----------|

**🧾 Sub-entregable:**  
**Sensor Gateway** — MCU ↔ PC + GUI + visión simple + inferencia ML ligera.

---

## 🧮 Evaluaciones y Tests Finales (Semana 12)

| Tipo de test | Objetivo | Herramientas recomendadas |
|---------------|-----------|---------------------------|
|---------------|-----------|---------------------------|
| **Seguridad embebida** | Detectar fugas, desbordes y condiciones de carrera. | Valgrind · ThreadSanitizer · doctest |
|---------------|-----------|---------------------------|
| **Eficiencia** | Medir uso de memoria, tamaño binario y consumo MCU. | `perf` · `gprof` · STM Cube Monitor |
|---------------|-----------|---------------------------|
| **Performance** | Validar tiempos de respuesta, jitter, FPS y estabilidad PID. | Osciloscopio / simulador + logs CSV |
|---------------|-----------|---------------------------|

**📦 Entregable Final Trimestral:**  
_Embedded Fundamentals Kit_  
- RAII Task Manager  
- PID Engine + Filtros  
- Sensor Gateway (UART ↔ GUI + Visión + TinyML)  
- Informe técnico con métricas de seguridad, eficiencia y performance  

---

## 🧩 Resumen de Tiempos Estimados

| Bloque | Total estimado | Dedicación semanal | RTOS / SO predominante |
|---------|----------------|--------------------|-------------------------|
|---------|----------------|--------------------|-------------------------|
| **Bloque 1 — C++20 Moderno** | 28 h | 7 h/semana | FreeRTOS · Zephyr · Linux |
|---------|----------------|--------------------|-------------------------|
| **Bloque 2 — Control Clásico** | 30 h | 7.5 h/semana | FreeRTOS · Mbed · Linux |
|---------|----------------|--------------------|-------------------------|
| **Bloque 3 — Comunicación · Visión · TinyML** | 36 h | 9 h/semana | Zephyr · Mbed · PREEMPT-RT |
|---------|----------------|--------------------|-------------------------|
| **➡ Total Trimestre** | **≈ 94 h** | **8–10 h/semana** | — |
|---------|----------------|--------------------|-------------------------|

---

## 🎯 Resultados Esperados

✅ Aplicar RAII, templates y multithreading en entornos embebidos.  
✅ Diseñar y evaluar control PID y filtros digitales.  
✅ Comunicar MCU ↔ PC y visualizar datos en GUI.  
✅ Ejecutar inferencia TinyML simple en C++20.  
✅ Validar seguridad, eficiencia y performance en código embebido real.  

---

