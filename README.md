# Análisis de Clientes y Transacciones Bancarias

## 📌 Descripción del proyecto
Proyecto de **análisis de datos utilizando SQL** sobre un **modelo relacional bancario**.  
La base de datos fue diseñada desde cero, se cargaron datos realistas y se desarrollaron consultas analíticas para analizar el comportamiento de clientes, el volumen transaccional, el uso de canales y oportunidades de cross-selling.

El objetivo del proyecto es simular un escenario real de análisis en una entidad bancaria y demostrar competencias prácticas en SQL aplicadas a preguntas de negocio.

---

## 🧱 Modelo de datos
El modelo relacional está compuesto por las siguientes tablas:

- **clientes**: información demográfica y segmentación de clientes (Retail / Premium).
- **cuentas**: cuentas bancarias asociadas a cada cliente.
- **transacciones**: movimientos financieros por cuenta.
- **productos**: catálogo de productos bancarios.
- **clientes_productos**: relación muchos-a-muchos entre clientes y productos.

El diseño respeta principios de **normalización** y utiliza claves primarias y foráneas para garantizar la integridad de los datos.

---

## 🛠️ Tecnologías utilizadas
- SQL (MySQL)
- DB Fiddle (entorno SQL online)
- GitHub
- MySQL 8.0

---

## 🔍 Conceptos SQL aplicados
- Diseño de tablas con claves primarias y foráneas
- JOINs entre múltiples tablas relacionadas
- Funciones de agregación (`SUM`, `AVG`, `COUNT`)
- `GROUP BY` y `HAVING`
- Subconsultas
- Common Table Expressions (CTEs)
- Funciones ventana (`RANK`)
- Consultas orientadas a negocio

---

## 📊 Preguntas de negocio analizadas
- ¿Qué clientes generan mayor volumen transaccional?
- ¿Cuál es el saldo promedio por segmento de cliente?
- ¿Qué canales concentran la mayor cantidad de operaciones?
- ¿Qué clientes Premium no tienen productos de inversión contratados?
- ¿Qué clientes presentan alta actividad transaccional pero bajo saldo promedio?

---

## 💡 Principales insights
- Los clientes **Premium** presentan saldos promedio significativamente mayores que los clientes Retail.
- El **canal Online** concentra la mayor cantidad y volumen de transacciones, evidenciando una fuerte adopción digital.
- Se identifican clientes con **alta actividad transaccional y bajo saldo promedio**, lo que representa oportunidades para ofrecer productos de crédito o inversión.
- Existen clientes Premium sin productos de inversión contratados, lo que sugiere oportunidades claras de **cross-selling**.

---

## 📂 Estructura del repositorio

banking_customer_transactions_analysis/
│
├── README.md
├── schema.sql -- Estructura de la base de datos (CREATE TABLE)
├── inserts.sql -- Carga de datos (INSERT INTO)
└── queries.sql -- Consultas analíticas


---

## 🔗 Demo del proyecto
DB Fiddle: *https://www.db-fiddle.com/f/wNo38u3DK2BBsiPr6WpumE/2*

---

## 👤 Autor
**Nicolás Casanova**

Data Analyst Jr. | SQL | Python

