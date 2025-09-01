# Taller de PCBs KiCAD — RAS x CERES
**Proyecto de taller (Carrito con ESP32-S3)** · 
23-09-2024: **RAS Day** 🎉

Este repo contiene el material del taller colaborativo **RAS x CERES** de diseño de PCBs en KiCAD:
- Proyecto KiCad listo para abrir (v8+).
- Librerías de símbolos y huellas *incluidas* (rutas relativas).
- Reglas de diseño (DRC) configurables para JLCPCB.
- Gerbers de ejemplo y BOM.

## 🧩 Hardware del proyecto
- **MCU:** ESP32-S3 DevKit C1 (módulo, footprint incluido).
- **IMU:** MPU6050 (módulo).
- **Motores:** Módulo **DRV8833** (Driver de Motores).
- **Expansión I²C:** 3 conectores **JST-XH 4 pines** (VCC, GND, SDA, SCL).
- **Power & Actuadores:**
  - Bornera de tornillo para **batería** (2 + 2 pines).
  - Borneras de tornillo para **motores** (2×2 pines o 2× de 2 pines).

> **Tip de ruta**: el ESP32-S3 DevKit C1 aquí se usa como *módulo* (no el chip suelto), para acelerar footprinting y montaje.

## ⚙️ Requisitos
- **KiCad 8.x** (recomendado).
- Sin dependencias externas: librerías incluidas y referenciadas de forma **relativa**.

## 🚀 Uso rápido
```bash
# 1) Clona
git clone https://github.com/<tu-org-o-user>/Taller-PCBs-KiCAD-RASxCERES.git
cd Taller-PCBs-KiCAD-RASxCERES
```
🧭 Flujo de trabajo en el taller

  1) Esquemático (.kicad_sch):
      Bloques: ESP32S3, DRV8833, I2C_Expanders (3× JST-XH 4p), Power, MPU6050, (opcional) Color.
  
  2) Net labels claras: I2C_SDA, I2C_SCL, M1_A, M1_B, M2_A, M2_B, VBAT, 5V, 3V3, GND.
  3) Asignación de huellas (ya pre-asignadas; revisar conflictos si cambias referencias).
  4) Reglas/DRC: cargar kicad/rules/jlcpcb.kicad_dru.
  5) Ruteo: intenta mantener I²C corto y motores con pistas anchas.
  6) Fabricación: exporta Gerbers a kicad/fabrication/ o usa los de ejemplo

🤝 Créditos

Taller colaborativo [(RAS)](https://www.instagram.com/ras_uniandes/?hl=en) x CERES [(@ceres.robotics)](https://www.instagram.com/ceres.robotics/?hl=en)

