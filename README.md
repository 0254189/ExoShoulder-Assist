# ExoShoulder Assist

Prototipo funcional de exoesqueleto de asistencia para hombro, desarrollado como proyecto de titulación en Ingeniería Mecatrónica en la Universidad Panamericana (Guadalajara).

## ¿Qué es?

Dispositivo portátil que detecta cuando el usuario intenta levantar el brazo y lo asiste mediante un motor eléctrico con engranajes, llevando el hombro de 0° a 90° de elevación. Diseñado para personas con movilidad reducida en el hombro.

## Arquitectura del sistema

| Subsistema | Componente | Descripción |
|---|---|---|
| Sensado | IMU BMI160 | Mide ángulo y velocidad angular del brazo vía I2C |
| Control | ESP32 + ESC ZTW Beatles G2 | Procesa señal y genera PWM proporcional al movimiento |
| Actuación | BLDC 6354-270KV + Cicloidal 15:1 | Motor con engranajes que multiplican la fuerza 15× |
| Seguridad | Kill-switch + Fusible 40A | Corte de energía en ≤ 1 s ante cualquier falla |

## Especificaciones

| Parámetro | Valor |
|---|---|
| Rango de movimiento | 0° – 90° |
| Torque de salida estimado | 2.64 N·m |
| Relación de reducción | 15:1 |
| Voltaje de operación | 24V (6S Li-ion) |
| Peso del prototipo | ~3 kg |
| Costo de fabricación | ~6,300 MXN |

## Reducción cicloidal

Basada en el diseño open-source de [Berkeley Humanoid Lite](https://lite.berkeley-humanoid.org/) (UC Berkeley), adaptada para acoplarse al motor BLDC 6354 y fabricarse en PETG mediante impresión 3D FDM. Las modificaciones principales fueron el ajuste del acople al eje del motor, la selección de rodamientos compatibles y la optimización de tolerancias para impresión en PETG.

## Estructura del repositorio

## Póster

Disponible en línea en: (https://0254189.github.io/ExoShoulder-Assist/)

## Autor

Iván Enrique Gutiérrez Orozco — Universidad Panamericana, 2026
Asesores: Oscar Sánchez Barba · Zyanya Orozco
