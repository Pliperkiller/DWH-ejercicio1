# 📘 Ejercicio Propuesto: Construcción de un Modelo Estrella para Análisis de Transacciones de Tarjetas

**Objetivo:** Diseñar y crear un esquema de base de datos en forma de modelo estrella que permita analizar las transacciones realizadas con tarjetas de crédito, clasificadas por cliente y categoría de consumo.

---

## 📝 Contexto del Negocio

Una entidad financiera desea analizar las compras realizadas por sus clientes con tarjeta de crédito. Cada transacción está asociada a una categoría de consumo (como supermercados, tecnología, restaurantes, etc.) y a un cliente. La entidad quiere construir un modelo que le permita hacer análisis como:

- Total de compras por cliente.
- Valor total de transacciones por ciudad o departamento.
- Cantidad de transacciones por categoría.

---

## 🧩 Tareas del Estudiante

1. **Diseño del modelo estrella:**
   - Identificar las **dimensiones** y la **tabla de hechos** a partir de la descripción del problema.
   - Dibujar un diagrama del modelo estrella.

2. **Creación de tablas en SQL:**
   - Crear las tablas `transaccion`, `cliente` y `categoria` .
   - Asegurar la integridad referencial entre las tablas mediante claves foráneas.
   - Crear índices para optimizar las búsquedas frecuentes.

3. **Carga de información desde archivo `bd.xlsx`:**
   - Usar **SSIS**, o un script en Python para cargar la información contenida en el archivo `bd.xlsx`.
   - El archivo contiene los datos para poblar las tablas `cliente`, `categoria` y `transaccion`.
   - Asegúrate de respetar los tipos de datos definidos y la integridad de claves foráneas al momento de hacer la carga.

4. **Validación del modelo:**
   - Verificar que el modelo permite responder preguntas como:
     - ¿Cuál fue el valor total de compras por cliente el último mes?
     - ¿En qué departamento se realizaron más compras en la categoría de tecnología?
     - ¿Qué clientes han realizado transacciones con tarjetas inactivas?

---

## 💡 Requisitos Técnicos del Modelo

- Todas las tablas deben tener una clave primaria.
- Las claves foráneas deben estar correctamente definidas.
- Se deben crear índices en las columnas más consultadas (identificación, código de categoría, fecha).
- La columna `identificacion` se usará como clave de negocio para clientes (no el ID).
- El modelo debe evitar duplicidad en claves naturales (identificación, código de categoría).

---
