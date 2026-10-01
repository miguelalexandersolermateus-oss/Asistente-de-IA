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

