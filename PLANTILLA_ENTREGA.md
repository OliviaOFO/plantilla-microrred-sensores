# Memoria Técnica: Propuesta de Red/Microrred de Sensores en la Edificación

**Asignatura:** Comunicaciones Electrónicas y Procesado de Datos (2026)  
**Grupo N°:** [Insertar Número]  
**Integrantes:**
* [Nombre Completo del Estudiante 1] - [Correo/ID]
* [Nombre Completo del Estudiante 2] - [Correo/ID]

---

## Bloque 1: Contexto y Justificación del Proyecto

### 1. Antecedentes y Necesidad del Estudio
*Justifique aquí detalladamente el motivo de la implementación de la microrred de sensores en la edificación elegida. ¿Qué problemática resuelve? (Ej: Eficiencia energética, monitorización de la calidad del aire, seguridad estructural, automatización HVAC, etc.).*

### 2. Descripción de la Edificación
* Detalle las características del entorno objeto de estudio:
  * **Tipo de edificación:** [Ej. Hospital, Hotel, Edificio de Oficinas, Vivienda Residencial]
  * **Uso actual:** [Describir el tipo de actividades que se realizan en el inmueble]
  * **Características físicas:** [Número de plantas, superficie en m², materiales estructurales predominantes que afecten la propagación de RF]
  * **Situación y Lugar:** [Dirección exacta, coordenadas o localidad, entorno urbano/rural]

### 3. Normativa Asociada
*Enumere y describa detalladamente las Normas UNE o los requisitos técnicos obligatorios exigidos según el tipo de obra y el país de aplicación (Ej: Normas UNE de calidad ambiental interior, Código Técnico de la Edificación (CTE), reglamentación de instalaciones eléctricas, etc.). Cada decisión de diseño debe alinearse con este marco legal.*

---

## Bloque 2: Ingeniería de Comunicaciones y Arquitectura

### 4. Estructura del Sistema de Monitorización
*Desarrolle de forma extensa el núcleo técnico de la red de telecomunicaciones:*
* **Estructura de la Red:** [Definir si es una variable puntual o una estructura compleja de red de sensores: topología en estrella, malla (mesh), árbol, híbrida].
* **Protocolo de Comunicaciones:** [Justificar la elección del protocolo: Zigbee, LoRaWAN, BLE, Modbus, BACnet, Wi-Fi, etc. considerando las características de la edificación].
* **Resolución del Sistema de Comunicaciones:** [Explique cómo se resuelven las distancias, atenuaciones por muros, interferencias electromagnéticas y pérdidas de propagación de las señales].
* **Tratamiento de Señales:** [Explicar los elementos estudiados para acondicionar y procesar los datos: técnicas de filtrado digital, etapas de amplificación, conversión analógica-digital (ADC), tasas de muestreo y técnicas para evitar el aliasing].

### 5. Situación de Medida y Variables Físicas
*Defina con claridad qué variables físicas se pretenden monitorizar de forma puntual o continua (Ej: Temperatura, concentración de CO₂, humedad relativa, iluminación, presencia, vibraciones, corriente eléctrica) y el porqué de su elección en este caso de estudio.*

---

## Bloque 3: Despliegue de Hardware y Ubicación

### 6. Parámetros a Monitorizar y Número de Sensores
*Especifique la cantidad de dispositivos que se van a desplegar según las necesidades del edificio:*

| Variable Física | Parámetro Técnico Relacionado | Cantidad de Sensores a Instalar | Frecuencia de Muestreo Recomendada |
| :--- | :--- | :---: | :---: |
| *Ej: Temperatura* | *Grados Celsius (°C)* | *12* | *Cada 10 minutos* |
| *Ej: Calidad de Aire* | *Partes por millón de CO₂ (ppm)* | *6* | *Cada 1 minuto* |
| | | | |

### 7. Tipos de Sensores y Especificaciones
*Detalle los modelos comerciales elegidos. Es obligatorio incluir enlaces web directos y activos a las especificaciones o datasheets del fabricante.*

* **Sensor 1: [Nombre de la Variable]**
    * **Modelo/Referencia:** [Ej. DHT22 / MQ-135]
    * **Fabricante:** [Ej. Adafruit / Texas Instruments]
    * **Enlace Técnico:** [Inserte aquí la URL del fabricante de forma directa]
* **Sensor 2: [Nombre de la Variable]**
    * **Modelo/Referencia:** ...
    * **Fabricante:** ...
    * **Enlace Técnico:** ...

### 8. Ubicación de los Sensores y Modelado en Planta
*Para cada sensor o nodo, detalle las condiciones de su despliegue físico:*
* **Zona de instalación:** [Especificar si es zona exterior, interior, salas críticas, pasillos, etc.]
* **Altura de colocación:** [Ej. A 1.5 metros del suelo, fijado en techo, etc., justificado según la variable].
* **Planos de Planta/Alzado:** *Guarde las imágenes en la carpeta local `/planos_ubicacion` y enlácelas aquí abajo utilizando el formato Markdown:*

    ![Plano de Distribución - Planta Baja](planos_ubicacion/ejemplo_plano_baja.png)

---

## Bloque 4: Procesado de Datos y Viabilidad Económica

### 9. Rangos de Medición y Operación
*Especifique el rango dinámico de trabajo requerido para cada sensor versus las capacidades reales del hardware seleccionado:*

| Sensor / Modelo | Rango Físico Requerido en la Edificación | Rango de Medición del Fabricante | Resolución / Precisión |
| :--- | :--- | :--- | :--- |
| *Ej: DHT22 (Temp)* | *15 °C a 40 °C* | *-40 °C a 80 °C* | *0.1 °C / ±0.5 °C* |
| | | | |

### 10. Alimentación Eléctrica del Sistema
*Clasifique detalladamente el método de suministro energético de los dispositivos instalados. Justifique la autonomía si se emplean sistemas inalámbricos o de batería.*
* **Nodos de Sensores Inalámbricos:** [Ej. Batería o conexión directa a la red, estimación de duración, uso de modos Sleep, etc.].
* **Elementos Centrales (Gateways/Concentradores):** [Ej. Conexión directa a la red eléctrica comercial].

### 11. Presupuesto Económico Estimado
*Presente el desglose financiero del proyecto comercial planteado (precios unitarios o una estimación general):*

| Descripción / Componente | Cantidad | Precio Unitario (€) | Subtotal (€) | Enlace de Referencia de Coste |
| :--- | :---: | :---: | :---: | :--- |
| *Ej: Sensor CO₂ MQ-135* | *6* | *4.50 €* | *27.00 €* | *[Enlace Tienda]* |
| *Ej: Concentrador Gateway* | *1* | *120.00 €* | *120.00 €* | *[Enlace Tienda]* |
| **Costo Total Estimado del Sistema** | | | **147.00 €** | |

---

## Cierre del Estudio

### 12. Conclusiones del Estudio
*Resuma las conclusiones técnicas del estudio, la viabilidad del sistema de comunicaciones propuesto, las limitaciones encontradas y las posibles mejoras futuras del sistema de monitorización.*

### 13. Bibliografía y Referencias
*Liste todas las fuentes consultadas siguiendo un formato normalizado (Ej: IEEE, APA). Incluya datasheets, normativas, libros de texto y artículos técnicos.*

* [1] [Autor/Organización]. *[Título del Documento]*. [Año]. Disponible en: [URL]
* [2] ...
