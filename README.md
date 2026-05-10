# 🏍️ Tacómetro Digital con ATmega328PB y Pantalla GC9A01

## 📌 Descripción

Este proyecto implementa un tacómetro digital en tiempo real utilizando un microcontrolador **ATmega328PB** y una pantalla TFT circular **GC9A01**.

El sistema detecta pulsos provenientes del motor, calcula las revoluciones por minuto (**RPM**) y las representa gráficamente mediante una aguja animada y una visualización numérica.

Además, el proyecto integra código en lenguaje ensamblador AVR para optimizar el cálculo de RPM y mejorar el rendimiento del sistema embebido.

---

# ✨ Características

- 📈 Medición de RPM en tiempo real
- 🖥️ Interfaz gráfica circular tipo tacómetro automotriz
- ⚡ Uso de interrupciones externas para alta precisión
- 🔥 Integración de lenguaje ensamblador AVR
- 🎯 Aguja digital animada
- 🚀 Refresco aproximado de 60 FPS
- 📟 Visualización numérica de RPM
- 🧠 Optimización matemática para sistemas embebidos

---

# 🧰 Hardware Utilizado

| Componente | Descripción |
|---|---|
| Microcontrolador | ATmega328PB |
| Pantalla | GC9A01 TFT Circular |
| Comunicación | SPI |
| Entrada de señal | Pulsos del motor / sensor |

---

# 📚 Librerías Utilizadas

```cpp
#include <SPI.h>
#include <Adafruit_GFX.h>
#include <Adafruit_GC9A01A.h>
#include <math.h>
```

---

# ⚙️ Funcionamiento General

```text
Motor genera pulsos
        ↓
Interrupción detecta señal
        ↓
Se mide el tiempo entre pulsos
        ↓
Código ASM calcula RPM
        ↓
Se suaviza la lectura
        ↓
Se actualiza la pantalla TFT
```

---

# 🔥 Integración con Ensamblador AVR

El proyecto utiliza una función escrita en ensamblador AVR para realizar el cálculo de RPM.

La rutina ensambladora implementa una división binaria de 32 bits utilizando registros AVR y operaciones de bajo nivel.

Esto permite:

- ⚡ Mayor velocidad de cálculo
- 🧠 Menor carga del microcontrolador
- 🚀 Mejor rendimiento en tiempo real

---

# 🧠 Conceptos Aplicados

- Programación embebida
- Interrupciones externas
- Comunicación SPI
- Programación gráfica
- Trigonometría aplicada
- Ensamblador AVR
- Optimización de rendimiento
- Sistemas en tiempo real

---

# 📂 Estructura del Proyecto

```text
Proyecto/
│
├── tacometro.ino
├── calculo.S
├── README.md
```
