# Libros & Bytes

**Sistema de gestión de inventario y simulador de compras **

Pequeña aplicación en Python para gestionar el inventario de una cadena de librerías y permitir a los usuarios simular compras desde la consola. Incluye control de stock, filtros por rango de precios, descuentos por autor y una factura final con totales y ahorro por descuentos.

---

## ❓ ¿Qué problema resuelve?

Una cadena de librerías pequeña necesita una forma simple de:
- Visualizar qué libros están disponibles.
- Permitir a clientes simular compras verificando stock.
- Aplicar descuentos especiales por autor.
- Generar una factura final que indique total de libros, monto pagado y ahorro por descuentos.

Este programa resuelve ese flujo básico sin interfaz gráfica, ideal para validar la lógica de negocio antes de construir una interfaz.

---

## ⚙️ ¿Cómo lo resuelve?

La versión actual implementa:

- Inventario como una **lista de diccionarios**, cada libro tiene: `titulo`, `autor`, `precio`, `stock`.
- Función `mostrar_libros_disponibles()` que recorre el inventario y muestra los libros con stock > 1.
- Filtrado por **rango de precios** (entrada mínima y máxima).
- Función `comprar_libros(titulo, cantidad, ...)` que:
  - Verifica existencia y stock suficiente.
  - Calcula subtotal, aplica descuento por autor (si corresponde) y actualiza stock.
  - Acumula totales (cantidad de libros, monto pagado y ahorro por descuentos).
- Bucle `while` tipo menú que permite al usuario repetir acciones hasta finalizar y generar la **factura final**.

**Comportamiento esperado:** al finalizar, se muestra el total de libros comprados, monto pagado y ahorro por descuentos.

---

## 🧠 Modelos / metodologías aplicadas

No se usan modelos de machine learning; se aplican técnicas de programación estructurada y principios básicos:

- **Estructuras de datos:** lista de diccionarios para inventario, diccionario para descuentos.
- **Control de flujo:** `for`, `if/elif/else`, `while`.
- **Validación de entrada:** try/except para manejar entradas numéricas inválidas.

---

## 📈 Interpretación de resultados

El programa no produce "modelos" sino efectos sobre el inventario y reportes numéricos:

- **Stock**: cada compra válida reduce la cantidad en el inventario (`stock`) del libro comprado.
- **Monto y descuentos**: si un autor está en la lista de descuentos, el sistema calcula el ahorro y lo resta del subtotal.
- **Factura final**: resume la cantidad total de artículos comprados, el monto total pagado (ya con descuentos) y el ahorro acumulado.

**Ejemplo simple (simulado):**
- Compras 2 copias de *Tokio Blues* (precio $15.500 c/u) y el autor tiene 10% de descuento:
  - Subtotal = 2 × 15500 = 31.000
  - Ahorro = 10% × 31.000 = 3.100
  - Total a pagar = 27.900
- El stock de *Tokio Blues* se reduce en 2 unidades.
- La factura final resume estos valores y acumula si haces varias compras.

**Casos manejados:**
- Intento de comprar más unidades de las que hay -> mensaje de error.
- Libro no encontrado -> mensaje de error.
- Entrada no numérica para cantidades/precios -> validación y mensaje de error.

---

