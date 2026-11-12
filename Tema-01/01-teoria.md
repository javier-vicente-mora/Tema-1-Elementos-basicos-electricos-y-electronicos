# 01. Desarrollo Teórico: Electricidad y Magnitudes Básicas

---

## 1. ¿Qué es la Electricidad?

### 1.1. La materia y la carga eléctrica
Para entender la electricidad, debemos empezar por los ladrillos con los que está construido todo el universo: **los átomos**.

Un átomo está formado por tres partículas principales:
* **Protones:** Tienen carga eléctrica positiva ($+$) y están fijos en el núcleo.
* **Neutrones:** No tienen carga (son neutros) y están en el núcleo.
* **Electrones:** Tienen carga eléctrica negativa ($-$) y giran alrededor del núcleo en órbitas exteriores.

```text
       [  Átomo  ]
      /     |     \
Protones Neutrones Electrones
  (+)       (0)        (-)
```

> 💡 **Concepto Clave:**
> La **electricidad** es el movimiento o flujo de electrones libres a través de un material conductor (como el cobre de los cables de un ordenador).

---

### 1.2. Materiales conductores y aislantes

En la informática trabajamos constantemente con dos tipos de materiales según cómo permiten el paso de la electricidad:

| Tipo de Material | ¿Qué es? | ¿Cómo funciona? | Ejemplo en informática |
| :--- | :--- | :--- | :--- |
| **Conductor** | Material que permite que los electrones se muevan fácilmente por su interior. | Sus átomos tienen electrones exteriores muy sueltos que saltan de un átomo a otro sin apenas resistencia. | Cobre de los cables, pistas de cobre de la placa base, oro de los contactos del procesador. |
| **Aislante** | Material que frena o impide el paso de la corriente eléctrica. | Sus átomos retienen con mucha fuerza sus electrones, impidiendo que se muevan. | Plástico que recubre los cables, la resina de la placa base (FR4), goma, cerámica. |

---

## 2. Las 4 Magnitudes Eléctricas Fundamentales

Para trabajar en el taller de montaje de ordenadores necesitas conocer cuatro magnitudes básicas. Piensa en la electricidad como un **circuito de agua** para entenderlas fácilmente:

```text
[ Tanque de Agua con Presión ]  <--->  Voltaje / Tensión (V)
[ Caudal de Agua por el Tubo ]  <--->  Intensidad / Corriente (I)
[ Estrechamiento en la Tubería ] <--->  Resistencia (R)
[ Trabajo realizado por el Agua ]<--->  Potencia (P)
```

---

### 2.1. Tensión o Voltaje ($V$)

1. **¿Qué es?** Es la fuerza o "presión" que empuja a los electrones a moverse a través del circuito eléctrico. También se llama *diferencia de potencial*.
2. **¿Para qué sirve?** Sirve para suministrar la energía que necesitan las piezas del ordenador para encenderse y funcionar.
3. **¿Cómo funciona?** A mayor voltaje, mayor es la fuerza con la que son empujados los electrones.
4. **¿Unidad de medida?** El **Voltio (V)**, en honor al físico Alessandro Volta.
5. **¿Dónde lo encontramos en un ordenador?**
   * En el enchufe de la pared de tu casa: **230 V** (corriente alterna).
   * En los cables internos que alimentan el disco duro o la placa base: **+12 V**, **+5 V** y **+3,3 V** (corriente continua).
6. **Ejemplo práctico:** Si la fuente de alimentación no entrega los $+12\text{ V}$ correctos a la tarjeta gráfica, esta no tendrá la fuerza suficiente para encenderse y la pantalla se quedará en negro.

---

### 2.2. Intensidad de Corriente ($I$)

1. **¿Qué es?** Es la cantidad de electrones que pasan por un punto determinado de un cable en un segundo. Es el "caudal" eléctrico.
2. **¿Para qué sirve?** Indica cuánta corriente está consumiendo un componente informático cuando trabaja.
3. **¿Cómo funciona?** Si un componente requiere más potencia (como un procesador ejecutando un juego exigente), absorberá un número mayor de electrones por segundo.
4. **¿Unidad de medida?** El **Amperio (A)**, en honor a André-Marie Ampère. En electrónica se usa mucho el **Miliamperio (mA)** ($1\text{ A} = 1000\text{ mA}$).
5. **¿Dónde lo encontramos en un ordenador?**
   * Un procesador moderno (CPU) puede llegar a consumir más de $50\text{ A}$ a pleno rendimiento.
   * Un puerto USB 3.0 entrega hasta $0,9\text{ A}$ ($900\text{ mA}$) para cargar tu teléfono móvil.
6. **Ejemplo práctico:** Si conectas demasiados discos duros externos a un solo puerto USB no alimentado, sobrepasarás el límite de amperios del puerto y los discos dejarán de funcionar.

---

### 2.3. Resistencia Eléctrica ($R$)

1. **¿Qué es?** Es la oposición o dificultad que ofrece un material o componente al paso de la corriente eléctrica.
2. **¿Para qué sirve?** Sirve para limitar el flujo de corriente, proteger componentes delicados y adaptar tensiones dentro de las placas electrónicas.
3. **¿Cómo funciona?** A mayor resistencia, pasan menos electrones por el circuito. Al oponerse al paso de los electrones, la resistencia transforma parte de la energía eléctrica en **calor**.
4. **¿Unidad de medida?** El **Ohmio ($\Omega$)**, en honor a Georg Simon Ohm.
5. **¿Dónde lo encontramos en un ordenador?**
   * En las pequeñas resistencias cerámicas soldadas en la superficie de la placa base (SMD).
   * En los cables (tienen una resistencia casi nula, pero no cero).
6. **Ejemplo práctico:** Un LED indicador de encendido del chasis requiere una resistencia colocada en serie. Sin esa resistencia, circularían demasiados amperios y el LED se quemaría instantáneamente.

---

### 2.4. Potencia Eléctrica ($P$)

1. **¿Qué es?** Es la cantidad total de energía eléctrica que consume o transforma un aparato informático en un tiempo determinado (normalmente en un segundo).
2. **¿Para qué sirve?** Permite saber cuánta energía necesita una máquina y calcular el consumo energético o la capacidad que debe tener la fuente de alimentación.
3. **¿Cómo funciona?** Se calcula multiplicando la tensión (voltios) por la intensidad (amperios): 
   $$\text{Potencia} = \text{Tensión} \times \text{Intensidad} \quad (P = V \times I)$$
4. **¿Unidad de medida?** El **Vatio (W)** o *Watt*, en honor a James Watt. En fuentes de alimentación se usa a menudo el **Kilovatio (kW)** ($1\text{ kW} = 1000\text{ W}$).
5. **¿Dónde lo encontramos en un ordenador?**
   * En la etiqueta de la fuente de alimentación (por ejemplo: **650 W**, **750 W**).
   * En el consumo del procesador (TDP): por ejemplo, un procesador de $65\text{ W}$.
6. **Ejemplo práctico:** Si montas un ordenador gamer con un procesador de $120\text{ W}$ y una tarjeta gráfica de $300\text{ W}$, necesitarás una fuente de alimentación de al menos $650\text{ W}$ para garantizar un margen de funcionamiento seguro.

---

## 3. Resumen de Magnitudes Eléctricas

| Magnitud | Símbolo | Unidad de Medida | Símbolo Unidad | Instrumento de Medida |
| :--- | :---: | :--- | :---: | :--- |
| **Tensión / Voltaje** | $V$ (o $U$) | Voltio | $\text{V}$ | Voltímetro (en paralelo) |
| **Intensidad** | $I$ | Amperio | $\text{A}$ | Amperímetro (en serie) |
| **Resistencia** | $R$ | Ohmio | $\Omega$ | Ohmetro (sin tensión) |
| **Potencia** | $P$ | Vatio | $\text{W}$ | Vatímetro / Cálculo |

---

## 4. La Ley de Ohm

La **Ley de Ohm** es la regla matemática fundamental de la electricidad. Establece la relación directa entre la tensión, la intensidad y la resistencia en un circuito eléctrico.

![Triángulo de la Ley de Ohm](./img/ley-ohm.png)
*(Esquema didáctico: Triángulo de la Ley de Ohm para memorizar las fórmulas V = I x R, I = V / R, R = V / I)*

### 4.1. La Fórmula Principal
$$\text{Tensión} = \text{Intensidad} \times \text{Resistencia} \quad \longrightarrow \quad V = I \times R$$

De esta fórmula se despejan las otras dos relaciones esenciales:

1. **Para calcular la Intensidad ($I$):**
   $$I = \frac{V}{R}$$
   *(Si aumentamos la tensión $V$, aumenta la corriente $I$. Si aumentamos la resistencia $R$, disminuye la corriente $I$.)*

2. **Para calcular la Resistencia ($R$):**
   $$R = \frac{V}{I}$$

---

### 4.2. Regla mnemotécnica: El Triángulo de Ohm

Para recordar fácilmente las fórmulas en los exámenes o en el taller, utiliza el triángulo:

```text
       / \
      / V \
     /-----\
    / I | R \
   /_________\
```

* **Tapa la $V$:** Te queda $I \times R$. ($V = I \times R$)
* **Tapa la $I$:** Te queda $\frac{V}{R}$. ($I = \frac{V}{R}$)
* **Tapa la $R$:** Te queda $\frac{V}{I}$. ($R = \frac{V}{I}$)

---

## 5. Tipos de Corriente Eléctrica: AC vs DC

En el mantenimiento de ordenadores trabajamos obligatoriamente con dos formas distintas de corriente eléctrica.

![Electricidad Básica y Corrientes](./img/electricidad-basica.png)
*(Esquema didáctico: Diferencia entre Corriente Alterna sinusoidal y Corriente Continua constante)*

---

### 5.1. Corriente Alterna (AC - Alternating Current)

1. **¿Qué es?** Es una corriente eléctrica en la que los electrones cambian de sentido de circulación constantemente a una velocidad muy elevada.
2. **¿Cómo funciona?** En Europa, la corriente cambia de dirección **50 veces por segundo** (frecuencia de **50 Hertzios - Hz**). Su forma gráfica es una onda senoidal.
3. **¿Dónde la encontramos?** En los enchufes de las viviendas y talleres (230 V CA / 50 Hz).
4. **¿Por qué se usa?** Porque es muy fácil y barata de transportar a través de grandes distancias desde las centrales eléctricas hasta las ciudades.

---

### 5.2. Corriente Continua (DC - Direct Current)

1. **¿Qué es?** Es una corriente en la que los electrones se mueven siempre en la **misma dirección**, desde el polo negativo hacia el polo positivo, manteniendo una tensión estable en el tiempo.
2. **¿Cómo funciona?** Su voltaje no cambia de polaridad; es una línea recta constante.
3. **¿Dónde la encontramos?** En las baterías, pilas, cargadores de portátil y en el **interior de todos los componentes de un ordenador** (placa base, CPU, RAM, discos duros).
4. **¿Por qué se usa en informática?** Porque los microchips informáticos necesitan voltajes fijos y precisos para procesar los ceros y unos ($0$ y $1$) de la información digital.

---

### 5.3. Tabla Comparativa: Corriente Alterna (AC) vs Corriente Continua (DC)

| Característica | Corriente Alterna (AC) | Corriente Continua (DC) |
| :--- | :--- | :--- |
| **Símbolo** | $\sim$ ó AC | $\dots$ / $=$ ó DC |
| **Dirección del flujo** | Cambia de sentido constantemente | Única dirección constante |
| **Voltaje típico** | $230\text{ V}$ (Red doméstica) | $+12\text{ V}$, $+5\text{ V}$, $+3,3\text{ V}$, $+1,2\text{ V}$ |
| **Origen** | Generadores en centrales eléctricas | Baterías, pilas, Fuentes de alimentación (PSU) |
| **Uso informático** | Entrada a la fuente de alimentación del PC | Funcionamiento de placa base, CPU, discos, USB |

---

## 6. Circuitos Eléctricos Básicos

Un **circuito eléctrico** es un camino cerrado por el que pueden circular los electrones. Consta como mínimo de:
1. **Generador:** Aporta la tensión (ej. pila o fuente de alimentación).
2. **Conductor:** Cable de cobre que transporta los electrones.
3. **Receptor:** Componente que aprovecha la electricidad (ej. ventilador, LED, disco duro).
4. **Elemento de control:** Permite o interrumpe el paso (ej. botón de encendido del chasis).

```text
 ( + ) --- [ Interruptor ] --- ( Receptor / LED ) --- ( - )
   |                                                    |
   +----------------- [ Generador / Pila ] -------------+
```

Existen tres configuraciones básicas:
* **Circuito en Serie:** Los receptores se conectan uno a continuación de otro. Si uno se rompe, el circuito se abre y nada funciona.
* **Circuito en Paralelo:** Cada receptor tiene su propio camino independiente. Si un componente se avería, los demás siguen recibiendo corriente. **¡Es el sistema utilizado en los ordenadores!**
* **Circuito Mixto:** Combina tramos en serie y tramos en paralelo.

---

## 📌 Resumen del Tema 01 (Teoría)

1. La **electricidad** es el movimiento de electrones libres a través de un conductor.
2. Las cuatro magnitudes clave son: **Tensión** ($V$, voltios), **Intensidad** ($I$, amperios), **Resistencia** ($R$, ohmios) y **Potencia** ($P$, vatios).
3. La **Ley de Ohm** ($V = I \times R$) relaciona tensión, corriente y resistencia en un circuito.
4. La **Potencia** se calcula mediante $P = V \times I$.
5. La red eléctrica entrega **Corriente Alterna (AC)** a $230\text{ V}$, pero los componentes internos del ordenador funcionan exclusivamente con **Corriente Continua (DC)** ($+12\text{ V}$, $+5\text{ V}$, $+3,3\text{ V}$).
