# 03. Ejemplos Prácticos y Medición con Polímetro

---

## 1. Ejemplos Resueltos de la Ley de Ohm y Potencia

En esta sección veremos problemas reales resueltos paso a paso con la estructura exigida en el aula de taller.

---

### 🧮 Ejemplo Práctico 1: Cálculo de Intensidad en un LED
**Enunciado:** Queremos conectar un LED indicador en el panel frontal del ordenador. El LED necesita una tensión de $2\text{ V}$ para funcionar y le colocamos en serie una resistencia protectora de $500\ \Omega$. Si la fuente le entrega $12\text{ V}$, la resistencia debe absorber los $10\text{ V}$ restantes. ¿Qué intensidad de corriente ($I$) circulará por la resistencia?

* **Paso 1: Identificar los datos del problema.**
  * Tensión en la resistencia ($V$) = $10\text{ V}$
  * Resistencia ($R$) = $500\ \Omega$
  * Intensidad ($I$) = ¿?

* **Paso 2: Seleccionar la fórmula adecuada.**
  * Aplicamos la Ley de Ohm para despejar la Intensidad:
    $$I = \frac{V}{R}$$

* **Paso 3: Sustituir los valores y calcular.**
  $$I = \frac{10\text{ V}}{500\ \Omega} = 0,02\text{ Amperios}$$

* **Paso 4: Convertir a unidades comprensibles.**
  $$0,02\text{ A} \times 1000 = 20\text{ mA (Miliamperios)}$$

* **Solución Justificada:** Por la resistencia y el LED circulará una corriente de **$20\text{ mA}$**, valor totalmente seguro para no quemar el diodo LED.

---

### 🧮 Ejemplo Práctico 2: Cálculo de Resistencia de un Ventilador
**Enunciado:** Un ventilador de chasis funciona conectado a un raíl de $+12\text{ V}$ de la fuente de alimentación y consumiendo una corriente de $0,3\text{ A}$. ¿Cuál es la resistencia interna ($R$) del motor del ventilador?

* **Paso 1: Identificar datos.**
  * $V = 12\text{ V}$
  * $I = 0,3\text{ A}$
  * $R = ¿?$

* **Paso 2: Aplicar la fórmula.**
  $$R = \frac{V}{I}$$

* **Paso 3: Operar.**
  $$R = \frac{12\text{ V}}{0,3\text{ A}} = 40\ \Omega$$

* **Solución Justificada:** La resistencia eléctrica interna del devanado del ventilador es de **$40\ \Omega$**.

---

### 🧮 Ejemplo Práctico 3: Dimensionamiento de una Fuente de Alimentación
**Enunciado:** Vamos a ensamblar un ordenador de oficina con los siguientes componentes y consumos en el raíl de $+12\text{ V}$:
* Procesador (CPU): $65\text{ W}$
* Placa Base: $25\text{ W}$
* Memoria RAM y SSD: $15\text{ W}$
* Ventiladores y periféricos: $15\text{ W}$

¿Cuánta intensidad ($I$) en amperios demandará el ordenador a la línea de $+12\text{ V}$ y cuál será la potencia total requerida?

* **Paso 1: Sumar la potencia total consumida ($P_{total}$).**
  $$P_{total} = 65\text{ W} + 25\text{ W} + 15\text{ W} + 15\text{ W} = 120\text{ W}$$

* **Paso 2: Calcular la intensidad total demandada en $+12\text{ V}$.**
  * Despejamos $I$ de la fórmula de la potencia ($P = V \times I$):
    $$I = \frac{P}{V}$$
  * Sustituimos valores:
    $$I = \frac{120\text{ W}}{12\text{ V}} = 10\text{ Amperios}$$

* **Paso 3: Aplicar un margen de seguridad.**
  * En montaje informático se aconseja añadir un **$20\%-30\%$ de margen** para garantizar que la fuente no trabaje al límite térmico.
    $$\text{Potencia recomendada} = 120\text{ W} \times 1,30 = 156\text{ W}$$

* **Solución Justificada:** El equipo consumirá **$10\text{ A}$** en la línea de $+12\text{ V}$. Con una fuente básica de $300\text{ W}$ o $400\text{ W}$ el ordenador funcionará de forma óptima y sobrada.

---

## 2. Guía de Uso del Polímetro / Multímetro Digital

El **Polímetro** o **Multímetro** es la herramienta imprescindible de cualquier técnico informático para diagnosticar fallos en fuentes de alimentación, comprobar cables roto o verificar el estado de componentes.

```text
       +-------------------------+
       |   [ 12.04 V ] (Pantalla)|
       +-------------------------+
       |                         |
       |       (   (O)   )       | <- Selector Rotativo
       |     OFF  V=   V~        |
       |      A=       $\Omega$   |
       |                         |
       |  [10A]  [COM]  [V/$\Omega$]  | <- Clavijas de Entrada
       +-------------------------+
```

---

### 2.1. Partes del Multímetro Digital

1. **Pantalla Display LCD:** Muestra el valor numérico de la medición y la unidad.
2. **Rueda / Selector Rotativo:** Permite elegir qué magnitud medir ($V=$, $V\sim$, $A$, $\Omega$) y la escala.
3. **Clavija COM (Común):** Aquí se conecta **SIEMPRE el cable NEGRO** (masa / tierra).
4. **Clavija $V/\Omega/\text{mA}$:** Aquí se conecta el **cable ROJO** para medir tensión, resistencia o pequeñas corrientes.
5. **Clavija 10A / 20A:** Clavija especial para medir grandes intensidades de corriente (cable rojo).

---

### 2.2. Procedimiento 1: Medir Tensión en Corriente Continua (DC)
* **Objetivo:** Comprobar si la fuente de alimentación del ordenador está entregando exactamente $+12\text{ V}$ en un conector Molex.

```text
 [ Cable Rojo Polímetro ]  ---> Pin Amarillo (+12V Molex)
 [ Cable Negro Polímetro ] ---> Pin Negro (Masa Molex)
```

1. Coloca el **cable negro** en el puerto `COM` y el **cable rojo** en el puerto `V/\Omega`.
2. Gira el selector del multímetro a **Tensión Continua ($V\dots$ ó $DCV$)** en la escala de **$20\text{ V}$**.
3. Enciende la fuente de alimentación del PC.
4. Introduce la punta **roja** en el orificio del **cable amarillo** del Molex ($+12\text{ V}$) y la punta **negra** en el orificio del **cable negro** (Masa).
5. **Lectura esperada:** En la pantalla debe aparecer un valor entre **$11,4\text{ V}$ y $12,6\text{ V}$** (margen de tolerancia del $\pm 5\%$).
   * *Si la pantalla marca $0\text{ V}$:* La fuente está apagada, averiada o el raíl está cortocircuitado.

---

### 2.3. Procedimiento 2: Medir Resistencia Eléctrica
* **Objetivo:** Averiguar el valor real de una resistencia de la placa base o comprobar un componente pasivo.

> ⚠️ **REGLA DE ORO DE SEGURIDAD:**
> **NUNCA midas resistencia en un circuito que tenga corriente eléctrica.** Desconecta siempre el equipo de la red eléctrica antes de tocar las puntas.

1. Desconecta el equipo de la pared.
2. Coloca el selector en **Resistencia ($\Omega$)**.
3. Si el multímetro no es autorrango, selecciona la escala inmediatamente superior al valor estimado (ejemplo: escala de $2\text{ k}\Omega$ para medir una resistencia de $1000\ \Omega$).
4. Toca con la punta roja un extremo del componente y con la negra el otro extremo.
5. **Lectura:** Compara el valor obtenido en pantalla con las bandas de colores del componente.

---

### 2.4. Procedimiento 3: Prueba de Continuidad Acústica
* **Objetivo:** Comprobar si un cable de alimentación está partido por dentro o si un fusible está quemado.

1. Ajusta el selector en la posición de **Continuidad** (representada por el icono de un altavoz o diodo $\rightarrow\ \ \mathbf{o)))$}$).
2. Junta las dos puntas de prueba (roja y negra). El multímetro debe emitir un **pitido continuo** y marcar un valor cercano a $0\ \Omega$.
3. Para comprobar un cable: pon la punta roja en un extremo del cable y la negra en el extremo opuesto del mismo hilo.
4. **Interpretación:**
   * **¡SUENA PITIDO!** $\rightarrow$ El cable está sano y la corriente pasa perfectamente.
   * **SILENCIO (marca "OL" ó "1"):** $\rightarrow$ El cable está **cortado** interiormente o el fusible está **fundido**. Hay que sustituirlo.

---

## 🛡️ Normas de Seguridad Eléctrica en el Taller de Informática

1. **Desconexión Total:** Antes de abrir la caja de un ordenador o manipular componentes internos, desconecta siempre el cable de alimentación de la toma de corriente de la pared.
2. **Descarga de Condensadores:** Las fuentes de alimentación retienen voltajes peligrosos en sus grandes condensadores incluso minutos después de desenchufadas. **Nunca abras la carcasa metálica de una fuente de alimentación.**
3. **Electricidad Estática (ESD):** La carga estática de tu cuerpo puede destruir los microchips. Toca una superficie metálica sin pintar del chasis antes de manipular las piezas o usa una pulsera antiestática.
4. **Aislamiento de Herramientas:** Utiliza destornilladores y Alicates con mango de goma aislante certificado.
