# 02. Componentes Electrónicos y Fuentes de Alimentación

---

## 1. Clasificación: Electrónica Pasiva vs Activa

En la placa base, tarjeta gráfica y fuente de alimentación de un ordenador conviven miles de componentes electrónicos diminutos. Se dividen en dos gran categorías:

![Componentes Electrónicos](./img/componentes-electronicos.png)
*(Esquema didáctico: Galería visual de componentes pasivos y activos en placas informáticas)*

| Categoría | ¿Qué son? | Función principal | Ejemplos |
| :--- | :--- | :--- | :--- |
| **Componentes Pasivos** | Componentes que no pueden controlar la corriente por sí mismos ni amplificar señales. Se limitan a almacenar, liberar o frenar la energía. | Limitar corriente, filtrar interferencias, almacenar pequeñas cargas. | Resistencias, Condensadores, Bobinas (Inductores). |
| **Componentes Activos** | Componentes fabricados con materiales semiconductores (silicio) capaces de controlar, conmutar o amplificar el flujo de corriente. | Actuar como interruptores ultrasónicos, regular voltajes y procesar datos. | Diodos, LEDs, Transistores (MOSFET), Circuitos Integrados (Chips). |

---

## 2. Componentes Pasivos

### 2.1. Las Resistencias (Resistores)

1. **¿Qué es?** Es un componente diseñado para oponerse al paso de la corriente eléctrica.
2. **¿Para qué sirve?** Limita la intensidad para proteger otros componentes sensibles (como LEDs) y divide voltajes dentro de los circuitos de la placa base.
3. **¿Cómo funciona?** Convierte el exceso de energía eléctrica en calor.
4. **¿Dónde las encontramos?** 
   * En formato tradicional cilíndrico con bandas de colores en circuitos antiguos o fuentes de alimentación.
   * En formato **SMD** (Surface Mount Device - Montaje en Superficie): diminutos rectángulos negros soldados directamente sobre la placa base con un número grabado arriba.

#### El Código de Colores de las Resistencias
Las resistencias tradicionales utilizan 4 bandas de colores para indicar su valor en Ohmios ($\Omega$):

```text
  Bandas:  [ 1ª ] [ 2ª ] [ Multiplicador ]   [ Tolerancia ]
           Dígito Dígito  x 10^N              ±%
```

| Color | 1ª y 2ª Banda (Dígito) | 3ª Banda (Multiplicador) | 4ª Banda (Tolerancia) |
| :--- | :---: | :---: | :---: |
| **Negro** | 0 | $\times 1$ | - |
| **Marrón** | 1 | $\times 10$ | $\pm 1\%$ |
| **Rojo** | 2 | $\times 100$ | $\pm 2\%$ |
| **Naranja** | 3 | $\times 1.000$ ($1\text{ k}\Omega$) | - |
| **Amarillo** | 4 | $\times 10.000$ | - |
| **Verde** | 5 | $\times 100.000$ | - |
| **Azul** | 6 | $\times 1.000.000$ ($1\text{ M}\Omega$) | - |
| **Dorado** | - | $\times 0,1$ | $\pm 5\%$ |
| **Plateado**| - | $\times 0,01$ | $\pm 10\%$ |

* **Ejemplo resuelto:** Resistencia con bandas **Marrón - Negro - Rojo - Dorado**
  * 1ª Banda (Marrón): `1`
  * 2ª Banda (Negro): `0` $\rightarrow$ Valor base: `10`
  * 3ª Banda (Rojo): Multiplicador $\times 100$
  * 4ª Banda (Dorado): Tolerancia $\pm 5\%$
  * **Resultado:** $10 \times 100 = 1000\ \Omega = 1\text{ k}\Omega\ (\pm 5\%)$

---

### 2.2. Los Condensadores (Capacitores)

1. **¿Qué es?** Es un componente capaz de **almacenar energía eléctrica** en forma de campo eléctrico y liberarla muy rápidamente cuando la red la necesita.
2. **¿Para qué sirve?** Filtra los rizos de la corriente, estabiliza el voltaje que llega al procesador y amortigua los picos de tensión.
3. **¿Cómo funciona?** Consta de dos placas conductoras separadas por un material aislante (dieléctrico).
4. **¿Unidad de medida?** El **Faradio (F)**. Como el Faradio es gigantesco, se usan microfaradios ($\mu\text{F}$), nanofaradios ($\text{nF}$) o picofaradios ($\text{pF}$).
5. **¿Dónde los encontramos?**
   * **Condensadores Electrolíticos:** Cilindros con polaridad ($+$ y $-$). Tienen una franja blanca que marca la pata negativa. Se ven mucho en fuentes de alimentación y placas base.
   * **Condensadores Sólidos (Polímero):** De mayor calidad, no explotan ni se hinchan con el calor.
6. **⚠️ Avería típica en informática (Condensador hinchado):**
   * Si un condensador electrolítico sobrepasa su temperatura máxima, la parte superior de aluminio se abomba (se hincha) o suelta un líquido marrón. Un condensador hinchado en una placa base provoca reinicios aleatorios o que el ordenador no encienda.

---

### 2.3. Bobinas o Inductores (Chokes)

1. **¿Qué es?** Es un componente formado por un hilo de cobre enrollado en espiral alrededor de un núcleo de ferrita.
2. **¿Para qué sirve?** Almacena energía en forma de **campo magnético** y frena los cambios bruscos de corriente de alta frecuencia.
3. **¿Dónde los encontramos?** En la zona del **VRM** (Módulo Regulador de Voltaje) que rodea al procesador en la placa base. Son unos cubitos negros o grises sellados marcados como "R47" o "1R0".

---

## 3. Componentes Activos

### 3.1. Diodos y LEDs

1. **¿Qué es?** Es un componente semiconductor de dos patillas (Ánodo $+$ y Cátodo $-$) que permite el paso de la corriente en **una sola dirección** y la bloquea en sentido contrario.
2. **¿Para qué sirve?** Protege los circuitos informáticos contra inversiones accidentales de polaridad y convierte Corriente Alterna en Continua.
3. **Diodo LED (Light Emitting Diode):** Es un diodo especial que emite luz visible cuando circula corriente por él.
4. **¿Dónde los encontramos?**
   * LEDs de encendido (PWR_LED) y de actividad del disco duro (HDD_LED) en el chasis del ordenador.
   * Iluminación RGB y diodos de diagnóstico de fallos (EZ Debug LED) en placas base modernas.

---

### 3.2. Los Transistores y el MOSFET

1. **¿Qué es?** Es el componente electrónico más importante del mundo moderno. Es un interruptor electrónico ultrasónico sin partes mecánicas.
2. **¿Para qué sirve?** Permite encender o apagar la corriente millones o miles de millones de veces por segundo mediante una pequeña señal de control.
3. **El transistor MOSFET (Metal-Oxide-Semiconductor Field-Effect Transistor):**
   * Es el tipo de transistor utilizado masivamente en informática.
   * **¿Dónde lo encontramos?** En los circuitos VRM de la placa base para alimentar la CPU y la RAM, y por miles de millones dentro del propio chip del microprocesador.

---

### 3.3. Circuitos Integrados (Chips o Microchips)

1. **¿Qué es?** Una pastilla diminuta de silicio que contiene en su interior miles, millones o miles de millones de transistores, resistencias y diodos miniaturizados en un solo bloque.
2. **¿Dónde los encontramos?**
   * El Microprocesador (CPU).
   * Los chips de memoria RAM y almacenamiento SSD.
   * El chipset de la placa base y el chip Super I/O (controlador de sensores y temperatura).

---

## 4. La Fuente de Alimentación Informática (PSU)

La **Fuente de Alimentación** (PSU - Power Supply Unit) es la encargada de transformar la corriente peligrosa e inestable del enchufe de pared ($230\text{ V}$ CA) en los voltajes continuos seguros ($+12\text{ V}$, $+5\text{ V}$, $+3,3\text{ V}$ DC) que necesita el PC.

```text
  230V AC  --->  [ Transformación ] ---> [ Rectificación ] ---> [ Filtrado ] ---> [ Estabilización ] ---> Voltajes DC PC
 (Pared)         (Bajar Voltaje)        (AC a DC)              (Alisar onda)     (Voltaje exacto)    (+12V, +5V, +3.3V)
```

---

### 4.1. Las 4 Etapas de Conversión de la Fuente

1. **Transformación:** Reduce la alta tensión de la red ($230\text{ V}$) a tensiones mucho más bajas.
2. **Rectificación:** Mediante diodos, convierte la Corriente Alterna (AC) en Corriente Continua pulsante.
3. **Filtrado:** Mediante grandes condensadores electrolíticos, alisa la corriente eliminando las fluctuaciones de onda.
4. **Estabilización / Regulación:** Entrega voltajes completamente planos, limpios y estables ante cualquier variación de consumo del ordenador.

---

### 4.2. Raíles de Voltaje y Sus Usos

La fuente de alimentación distribuye la energía a través de cables diferenciados por códigos de color estándar:

| Raíl de Voltaje | Color de cable habitual | Componentes informáticos que alimenta |
| :---: | :---: | :--- |
| **$+12\text{ V}$** | **Amarillo** | **El raíl más importante:** Alimenta el procesador (CPU), la tarjeta gráfica (GPU), ventiladores y motores de discos duros. |
| **$+5\text{ V}$** | **Rojo** | Chips lógicos de placas base, discos SSD SATA de $2.5"$, electrónica interna de discos y puertos USB. |
| **$+3,3\text{ V}$** | **Naranja** | Ranuras de memoria RAM, chipsets de la placa base y tarjetas PCI Express. |
| **$+5\text{ VSB}$ (Standby)** | **Púrpura** | Mantiene con corriente la placa cuando el PC está apagado para permitir encenderlo mediante el botón del chasis o por red. |
| **Masa / Tierra ($0\text{ V}$)** | **Negro** | Cierre del circuito para todos los cables. |

---

### 4.3. Conectores Principales de la Fuente de Alimentación

```text
[ ATX 24 Pines ]    ---> Placa base principal
[ EPS 4+4 Pines ]   ---> Alimentación de la CPU
[ PCIe 6+2 Pines ]  ---> Tarjeta gráfica dedicada
[ SATA Power ]      ---> Discos duros HDD / SSD
[ Molex 4 Pines ]   ---> Ventiladores y periféricos antiguos
```

1. **Conector ATX Principal (20+4 pines):** Alimenta la electrónica general de la placa base.
2. **Conector EPS / ATX 12V (4+4 pines):** Aporta la energía dedicada exclusivamente al procesador.
3. **Conector PCIe (6+2 pines / 12VHPWR 12+4 pines):** Proporciona energía extra a las tarjetas gráficas dedicadas de alto rendimiento.
4. **Conector SATA Power (15 pines):** Forma de "L", alimenta discos duros HDD, unidades SSD y sistemas de refrigeración líquida.
5. **Conector Molex (4 pines):** Conector clásico grande, utilizado para ventiladores del chasis o accesorios secundarios.

---

### 4.4. Eficiencia Energética: Certificación 80 Plus

No toda la energía que entra a la fuente se aprovecha; parte se pierde en forma de calor. La certificación **80 Plus** garantiza que la fuente aprovecha al menos el $80\%$ de la energía de la pared:

* **80 Plus White:** $80\%$ de eficiencia mínima.
* **80 Plus Bronze:** $82\% - 85\%$ de eficiencia.
* **80 Plus Gold:** $87\% - 90\%$ de eficiencia (muy recomendada en montaje informático).
* **80 Plus Platinum / Titanium:** Más del $90\%$ de eficiencia (gama alta y servidores).
