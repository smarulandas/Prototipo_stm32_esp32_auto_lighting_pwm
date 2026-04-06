# Prototipo: Sistema de Detección Automática de Luz con STM32, ESP32 y Activación PWM de Faros en Ambientes Oscuros

## Descripción general
Este proyecto presenta el diseño de un sistema electrónico embebido capaz de detectar condiciones de baja iluminación ambiental y activar automáticamente una lámpara LED de 12V. El sistema fue desarrollado alrededor del microcontrolador **STM32F030C8T6**, integrando monitoreo local mediante pantalla LCD, retroalimentación visual con LEDs y notificación remota a través de un módulo **ESP32**.

## Objetivo
Diseñar e implementar un sistema embebido que detecte oscuridad ambiental y, en respuesta, accione automáticamente una lámpara LED de 12V, proporcionando información local y remota sobre el estado del sistema.

## Funcionamiento del sistema
El sistema opera de forma completamente automática. Un sensor **MH-SENSOR-SERIES** detecta niveles bajos de luz ambiente y envía una señal digital al **STM32F030C8T6**. El microcontrolador genera una señal **PWM** que controla un **MOSFET de canal N**, encargado de conmutar una lámpara LED de 12V. El estado del sistema se visualiza en una pantalla **LCD 16x2 con interfaz I2C** y también se transmite por **UART** al módulo **ESP32** para notificación vía Wi-Fi. Además, LEDs indicadores permiten identificar visualmente si la lámpara se encuentra encendida o apagada.

## Aplicaciones
Este proyecto puede aplicarse en sistemas automáticos de iluminación para vehículos, túneles, estacionamientos, zonas de baja visibilidad y otras soluciones de asistencia embebida orientadas a seguridad y automatización.

## Estado del proyecto
**Prototipo / RevA**

El objetivo principal de este trabajo fue el diseño e integración del sistema y la PCB en **Altium Designer**. Durante esta primera iteración se identificaron oportunidades de mejora en el diseño del esquemático, la ubicación de algunos componentes y el ruteo de la placa, las cuales quedan documentadas para una futura revisión **RevB**.

## Documentación
La documentación completa del proyecto se encuentra en:

- `docs/Sistema_de_Deteccion_Automatica_de_Luz.pdf`

Allí se incluyen:
- Introducción
- Objetivo
- Descripción general del sistema
- Componentes
- Modo de funcionamiento
- Power Budget
- Diagrama Funcional de Alto Nivel
- Aplicaciones del proyecto
- Cálculos para selección de componentes
- Lista de materiales (BOM)
- Integración con STM32CubeIDE
- Esquemáticos
- PCB 2D
- PCB 3D
- PCB Scale
- Conclusiones
- Bibliografía

## Herramientas y tecnologías utilizadas
- STM32F030C8T6
- ESP32
- PWM
- MOSFET de canal N
- LCD 16x2 con interfaz I2C
- UART
- Altium Designer
- STM32CubeIDE

## Mejoras futuras
- Revisión y corrección del esquemático.
- Optimización de la distribución de componentes en PCB.
- Mejora del ruteo de pistas.
- Generación de una nueva revisión de hardware (RevB).
