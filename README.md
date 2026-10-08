# Asistente-de-IA
El proyecto consiste en la creación de un asistente virtual basado en inteligencia artificial, diseñado para brindar apoyo a los usuarios de manera rápida, sencilla y personalizada. El asistente podrá comprender preguntas y solicitudes, proporcionar información, orientar al usuario en diferentes actividades y facilitar el acceso a recursos útiles.
## 1. Perfil del Agente
<img width="1829" height="564" alt="Captura de pantalla 2026-08-13 101533" src="https://github.com/user-attachments/assets/4ef94daf-ece2-4085-b26b-4e440880290c" />

## 2. Mapa de procesos(Conocimientos a apropiar)

<img width="1203" height="680" alt="image" src="https://github.com/user-attachments/assets/5a975ac9-0a01-4f86-96b6-79e54a092a35" />

## 3. Semana 4

<img width="1619" height="780" alt="image" src="https://github.com/user-attachments/assets/e70248ae-e84a-4bf3-9cea-253db691ea0a" />

<img width="431" height="666" alt="image" src="https://github.com/user-attachments/assets/c2a98257-2c67-48c9-a404-1e1e83ca0df4" />

## 4. semana 5

<img width="757" height="870" alt="image" src="https://github.com/user-attachments/assets/cb6797c0-f58a-4fa9-ba3a-64417641f8c9" />

##  Arquitectura de Atención

### ¿Qué es el filtro de atención?

FinUni utiliza un filtro de atención para identificar la información relevante para la administración financiera del estudiante. El sistema prioriza información relacionada con ingresos, egresos, ahorro, presupuesto y metas financieras.

###  Definición de "Ruido"

Se considera ruido toda información que no sea necesaria para analizar la situación financiera del estudiante.

Ejemplos:
- Conversaciones casuales.
- Información repetida.
- Información que no está relacionada con las finanzas.
- Datos que no aportan al análisis financiero.

###  Reglas de Atención

1. Si el mensaje contiene información sobre ingresos, egresos, ahorro o presupuesto, FinUni le dará prioridad alta.
2. Si el usuario realiza una pregunta financiera, FinUni debe procesarla como información prioritaria.
3. Si la información no está relacionada con las finanzas, se considera ruido.
4. Si falta un dato importante, FinUni debe solicitarlo al usuario.
5. Si el usuario expresa preocupación por su situación económica, FinUni debe adaptar su respuesta de manera empática.

###  Prioridad de información

| Información | Prioridad |
|---|---:|
| Ingresos | 5/5 |
| Egresos | 5/5 |
| Metas de ahorro | 5/5 |
| Presupuesto | 5/5 |
| Fechas de pagos | 4/5 |
| Estado emocional | 4/5 |
| Preguntas generales | 3/5 |
| Conversación casual | 1/5 |
| Información irrelevante | 0/5 |

###  Ejemplo

**Entrada:**

> "Hoy fui a la universidad y gasté $20.000 en transporte."

**Información relevante:**
- Valor: $20.000
- Categoría: Transporte
- Tipo: Egreso

**Resultado:**

> FinUni registra un egreso de $20.000 en la categoría transporte.
>
> 
>### semana 7

### Estructura de la Base de Conocimiento de FinUni

FinUni organizará su memoria a largo plazo en diferentes categorías para almacenar y consultar información financiera relevante de los estudiantes.

| Carpeta de Memoria | Tipo de información | Ejemplos |
|---|---|---|
| 👤 Perfil del estudiante | Datos personales y académicos | Edad, carrera, semestre, universidad |
| 💰 Ingresos | Fuentes de dinero | Salario, beca, ayuda familiar, emprendimiento |
| 💸 Egresos | Gastos del estudiante | Transporte, alimentación, matrícula, materiales |
| 🎯 Metas de ahorro | Objetivos financieros | Matrícula, computador, materiales, fondo de emergencia |
| 📊 Presupuesto | Planificación financiera | Presupuesto mensual, límites de gasto |
| 📈 Historial financiero | Datos anteriores | Ingresos, gastos y ahorros de meses anteriores |
| 🎓 Información universitaria | Gastos relacionados con estudios | Matrícula, semestre, libros, transporte |
| 🧠 Hábitos financieros | Comportamiento económico | Frecuencia de ahorro, gastos impulsivos, cumplimiento del presupuesto |
| 💡 Educación financiera | Conocimientos financieros | Ahorro, presupuesto, intereses, deudas |

## 🧠 Semana 8 — La RAM Cognitiva

### Memoria de Trabajo de FinUni

La memoria de trabajo de FinUni es el espacio temporal donde el asistente mantiene la información más importante de la conversación actual. Su función es permitir que FinUni pueda comprender el contexto y responder correctamente sin tener que consultar toda su memoria a largo plazo en cada momento.

### 📦 Ventana de Contexto

Para el diseño inicial de FinUni se establece una capacidad de **7 elementos relevantes**, tomando como referencia el modelo de memoria de trabajo **7 ± 2**.

Los elementos que FinUni prioriza son:

| Prioridad | Elemento | Ejemplo |
|---|---|---|
| 1 | 💰 Ingresos | Beca de $1.500.000 |
| 2 | 💸 Egresos | Transporte: $200.000 |
| 3 | 🎯 Meta financiera | Ahorrar para comprar un computador |
| 4 | 📊 Presupuesto | Presupuesto mensual de $1.000.000 |
| 5 | 💵 Ahorro actual | $250.000 ahorrados |
| 6 | 📅 Fecha o periodo | Gastos del mes actual |
| 7 | ❓ Consulta actual | "¿Cuánto puedo ahorrar este mes?" |

### 🧠 Funcionamiento

Cuando el usuario proporciona información, FinUni identifica los datos más importantes y los mantiene temporalmente en su memoria de trabajo.

Si la cantidad de información supera la capacidad establecida, FinUni debe priorizar los datos relacionados con la pregunta actual y con la situación financiera del estudiante.

### 🔄 Regla de Gestión de la RAM

> Si la memoria de trabajo alcanza su límite de 7 elementos, FinUni deberá conservar los datos más relevantes para la consulta actual y desplazar la información menos importante o que haya dejado de ser necesaria.

### 💡 Ejemplo

**Usuario:**

"Recibí una beca de $1.500.000, mi familia me ayuda con $300.000 y este mes gasto $200.000 en transporte. Quiero ahorrar para comprar un computador."

FinUni identifica y mantiene temporalmente:

- 💰 Beca: $1.500.000
- 💰 Ayuda familiar: $300.000
- 💸 Transporte: $200.000
- 🎯 Meta: computador

Estos datos pueden utilizarse para calcular el presupuesto y generar recomendaciones de ahorro.

### 🎯 Objetivo

La memoria de trabajo permite que FinUni mantenga el contexto necesario durante una conversación, evitando sobrecargar el sistema con información irrelevante.

## 📚 Semana 9 — El Bibliotecario

### Sistema de Recuperación de Memoria de FinUni

El Bibliotecario es el mecanismo encargado de recuperar información almacenada en la memoria a largo plazo cuando FinUni necesita un dato que ya no se encuentra disponible en su memoria de trabajo.

Su función es conectar la memoria de trabajo (RAM) con la memoria a largo plazo (LTM).

### 🔎 Proceso de Recuperación

Cuando el usuario realiza una pregunta, FinUni sigue el siguiente proceso:

1. Recibe la pregunta del usuario.
2. Analiza qué información necesita para responder.
3. Comprueba si la información está disponible en la memoria de trabajo.
4. Si está disponible, utiliza directamente la información.
5. Si no está disponible, realiza una búsqueda en la memoria a largo plazo.
6. Recupera la información relevante.
7. Envía la información recuperada a la memoria de trabajo.
8. Procesa la información.
9. Genera la respuesta para el usuario.

### 🔄 Flujo de Recuperación

```text
USUARIO
   ↓
Pregunta
   ↓
Analizar información necesaria
   ↓
¿La información está en la RAM?
   ├── SÍ → Utilizar información → Generar respuesta
   │
   └── NO
        ↓
   Buscar en memoria a largo plazo
        ↓
   Recuperar información
        ↓
   Pasar información a la RAM
        ↓
   Procesar información
        ↓
   Generar respuesta
        ↓
      USUARIO

<img width="1063" height="443" alt="image" src="https://github.com/user-attachments/assets/35f1bf12-1204-4e00-af79-8094bbe9e370" />

