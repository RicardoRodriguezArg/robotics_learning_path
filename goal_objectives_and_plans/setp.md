# 🧩 Entorno de Desarrollo – Learning Path Full Stack Robotics

## 💻 Resumen General

- **Host OS:** Ubuntu (usás solo VMs o cross-compilación dentro de ellas).  
- **LPC1768:** ✔️ Sirve perfectamente para la **primera etapa** (C/C++, FreeRTOS, periféricos, comunicación).  
- **Hardware futuro:** Raspberry Pi 4/5 + STM32 Nucleo (F401RE/F446RE).  
- **Depurador recomendado:** J-Link EDU Mini + adaptador USB-UART.  
- **Enfoque:**  
  - VM1 → firmware MCU  
  - VM2 → Linux/ROS2/cross-compilación a ARM64  
  - VM3 (opcional) → IDEs propietarios (Windows)  

---

## 🖥️ VMs Recomendadas

> Usa **KVM/QEMU + virt-manager** (recomendado) o **VirtualBox**.  
> Mantén snapshots limpios y carpetas compartidas con tu host.

### 🧱 VM1 – “MCU-Dev” (Embebidos: LPC1768 / STM32)

| Recurso | Valor |
|----------|--------|
| **SO** | Ubuntu 22.04 LTS (mínimo 20.04) |
| **CPU/RAM/Disco** | 2 vCPU / 4–8 GB RAM / 40 GB |
| **Propósito** | Compilar, testear y flashear firmware bare-metal / FreeRTOS |

#### 📦 Paquetes principales
```bash
sudo apt update
sudo apt install -y build-essential git cmake ninja-build gdb-multiarch \
  python3-pip openocd minicom usbutils dfu-util clang-format ccache \
  libusb-1.0-0-dev gcc-arm-none-eabi gdb-arm-none-eabi

