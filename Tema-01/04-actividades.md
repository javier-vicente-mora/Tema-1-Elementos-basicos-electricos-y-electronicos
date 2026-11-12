# 04. Actividades Didácticas y Prácticas de Taller

---

## 📝 Bloque 1: Comprensión Teórica y Vocabulario Técnico

### Actividad 1.1: Relaciona cada Magnitud con su Medida
Relaciona mediante flechas o indicando la letra correspondiente en la tabla los elementos de la izquierda con su unidad de medida y símbolo correcto:

| Magnitud Eléctrica | Respuesta | Unidad de Medida | Símbolo |
| :--- | :---: | :--- | :---: |
| 1. Tensión o Voltaje | [   ] | A. Vatio | $\Omega$ |
| 2. Intensidad de Corriente | [   ] | B. Voltio | $\text{W}$ |
| 3. Resistencia Eléctrica | [   ] | C. Amperio | $\text{V}$ |
| 4. Potencia Eléctrica | [   ] | D. Ohmio | $\text{A}$ |

---

### Actividad 1.2: Verdadero o Falso Justificado
Indica si las siguientes afirmaciones son **Verdaderas (V)** o **Falsas (F)**. Si la afirmación es falsa, explica brevemente por qué.

1. `[   ]` La red eléctrica de nuestras casas entrega Corriente Continua (DC) a $230\text{ V}$.
2. `[   ]` Un material conductor es aquel que retiene con mucha fuerza sus electrones e impide el paso de la corriente.
3. `[   ]` Para medir resistencia con un polímetro, el equipo debe estar completamente desenchufado de la corriente eléctrica.
4. `[   ]` Un condensador electrolítico hinchado en la placa base es síntoma de que funciona correctamente.
5. `[   ]` El raíl de $+12\text{ V}$ de la fuente de alimentación del PC es el encargado de alimentar componentes de gran consumo como la CPU y la GPU.

---

### Actividad 1.3: Definiciones con tus Propias Palabras
Responde con frases sencillas y claras a las siguientes cuestiones:
1. ¿Por qué los ordenadores necesitan una Fuente de Alimentación si la corriente ya entra directamente desde el enchufe de la pared?
2. ¿Qué diferencia principal existe entre un componente electrónico **pasivo** (como una resistencia) y uno **activo** (como un transistor)?

---

## 🧩 Bloque 2: Identificación de Componentes y Fuentes

### Actividad 2.1: Código de Colores de Resistencias
Calcula el valor en Ohmios ($\Omega$) y la tolerancia de las siguientes resistencias utilizando la tabla de colores:

1. Resistencia A: **Rojo – Rojo – Marrón – Dorado**
   * Dígitos: _________
   * Multiplicador: _________
   * **Valor total:** ____________ $\Omega$ ($\pm$ _____%)

2. Resistencia B: **Amarillo – Violeta – Naranja – Dorado**
   * Dígitos: _________
   * Multiplicador: _________
   * **Valor total:** ____________ $\Omega$ ($\pm$ _____%)

3. Resistencia C: **Marrón – Negro – Amarillo – Plateado**
   * Dígitos: _________
   * Multiplicador: _________
   * **Valor total:** ____________ $\Omega$ ($\pm$ _____%)

---

### Actividad 2.2: Identificación de Conectores de Fuente de PC
Asocia cada conector de la fuente de alimentación con el componente al que da servicio:

| Conector | Opción | Componente del Ordenador |
| :--- | :---: | :--- |
| 1. Conector ATX 24 Pines | [   ] | A. Tarjeta gráfica dedicada de alto consumo (GPU). |
| 2. Conector EPS / ATX 12V (4+4 pines) | [   ] | B. Disco duro sólido (SSD) o disco mecánico moderno. |
| 3. Conector PCIe (6+2 pines) | [   ] | C. Placa base principal. |
| 4. Conector SATA Power (15 pines) | [   ] | D. Alimentación dedicada exclusivamente al procesador (CPU). |

---

## 🧮 Bloque 3: Ejercicios Numéricos de Ley de Ohm y Potencia

Completa las siguientes plantillas paso a paso aplicando las fórmulas aprendidas:

### Ejercicio 3.1: Cálculo de Intensidad
Una tira de iluminación LED interna para la caja del ordenador funciona a una tensión de $+12\text{ V}$ y presenta una resistencia interna de $24\ \Omega$. ¿Qué intensidad de corriente ($I$) consumirá la tira LED?

* **Fórmula:** $I = \frac{V}{R}$
* **Sustitución:** $I = \frac{\qquad\text{ V}}{\qquad\ \Omega}$
* **Resultado:** $I = \qquad\text{ Amperios}$.

---

### Ejercicio 3.2: Cálculo de Tensión
Por una resistencia de $100\ \Omega$ de un circuito de control pasa una corriente de $0,05\text{ A}$. ¿Qué tensión o caída de voltaje ($V$) existe en los extremos de la resistencia?

* **Fórmula:** $V = I \times R$
* **Sustitución:** $V = \qquad\text{ A} \times \qquad\ \Omega$
* **Resultado:** $V = \qquad\text{ Voltios}$.

---

### Ejercicio 3.3: Cálculo de Potencia y Elección de Fuente
Un alumno de Grado Básico quiere ensamblar un ordenador gaming con los siguientes consumos estimados a máximo rendimiento:
* Procesador: $105\text{ W}$
* Tarjeta Gráfica dedicada: $220\text{ W}$
* Placa base, RAM y SSD: $55\text{ W}$
* Ventiladores y luces RGB: $20\text{ W}$

1. Calcula la **potencia total consumida ($P_{total}$)** por todos los componentes.
2. Si aplicamos un **margen de seguridad del $25\%$**, ¿de cuántos Vatios ($W$) debe ser la fuente de alimentación como mínimo?
3. Entre las siguientes fuentes disponibles en el taller, ¿cuál elegirías? Justifica tu respuesta:
   * Option A: Fuente genérica de $350\text{ W}$.
   * Option B: Fuente 80 Plus Bronze de $550\text{ W}$.
   * Option C: Fuente 80 Plus Gold de $750\text{ W}$.

---

## 🛠️ Bloque 4: Supuestos Prácticos de Diagnóstico en Taller

### Supuesto Práctico 1: El PC no Enciende nada
**Situación:** Un cliente trae al taller un ordenador de sobremesa que no hace absolutamente nada al pulsar el botón de encendido: no gira ningún ventilador ni se enciende ningún LED.

**Cuestiones de Diagnóstico:**
1. Mencióna las dos primeras comprobaciones básicas de seguridad que debes hacer antes de desmontar piezas.
2. Si vas a medir la tensión de la toma de corriente de la pared con el polímetro, ¿en qué posición del selector debes colocar el multímetro ($V\sim$ CA o $V\dots$ CC)?
3. Al comprobar con la prueba de continuidad el cable de corriente que va del enchufe a la fuente, el polímetro marca "OL" y no emite ningún sonido. ¿Qué avería presenta el cable y cómo se soluciona?

---

### Supuesto Práctico 2: Reinicios Inesperados
**Situación:** Al abrir un PC que se reinicia solo al cabo de 10 minutos de uso, el técnico observa a simple vista que tres condensadores electrolíticos cilíndricos situados cerca del zócalo del procesador están abombados en la parte superior.

**Cuestiones:**
1. ¿Qué función realizan esos condensadores cerca del procesador?
2. ¿Por qué la deformación en la parte superior indica que el condensador está roto?
3. ¿Cuál es la solución técnica recomendada?

---

## 🔬 Bloque 5: Práctica Guiada de Taller (Paso a Paso)

### 📌 Práctica 1: Verificación de Voltajes en una Fuente ATX

**Material necesario:**
* Fuente de alimentación de ordenador (PSU).
* Polímetro digital con puntas de prueba.
* Clip o puente metálico aislado (para puentear el encendido de la fuente).
* Ficha de registro de datos.

```text
  [ Puente con Clip ]  ---> Pin Verde (PS_ON) + Pin Negro (GND) en ATX 24p
```

**Pasos a realizar por el alumnado:**
1. **Puentear la fuente:** Para encender la fuente fuera del PC, conecta un extremo de un clip en el **pin Verde (PS_ON)** del conector ATX de 24 pines y el otro extremo en cualquier **pin Negro (GND)**. Enchufa la fuente a la red. El ventilador de la fuente comenzará a girar.
2. **Configurar el polímetro:** Pon el selector en **$V\dots$ (DC)** escala de **$20\text{ V}$**. Punta negra en clavija `COM` y punta roja en `V/\Omega`.
3. **Realizar las mediciones** introduciendo la punta negra en un pin negro del conector Molex y la punta roja en los pins especificados en la tabla:

| Cable medido | Pin del conector | Voltaje Teórico | Voltaje Medido con Polímetro | ¿Está dentro de tolerancia ($\pm 5\%$)? |
| :---: | :---: | :---: | :---: | :---: |
| **Amarillo** | Molex Pin 1 | $+12,0\text{ V}$ | _______ V | [ Sí ] / [ No ] |
| **Rojo** | Molex Pin 4 | $+5,0\text{ V}$ | _______ V | [ Sí ] / [ No ] |
| **Naranja** | ATX 24p | $+3,3\text{ V}$ | _______ V | [ Sí ] / [ No ] |
| **Púrpura** | ATX 24p Pin 9 | $+5,0\text{ V}$ (SB) | _______ V | [ Sí ] / [ No ] |

4. **Conclusión final del alumno:** ¿Es apta esta fuente para ser instalada en un equipo informático? Explica por qué.
