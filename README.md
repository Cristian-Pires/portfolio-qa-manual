# 🛠️ Portfolio de QA Manual - Auditoría en SauceDemo

Este repositorio contiene la documentación técnica, diseño de casos de prueba y reportes de errores críticos hallados durante la auditoría de calidad realizada en la plataforma de prácticas **SauceDemo**.

---

### 📝 1. Planificación y Casos de Prueba
* **Objetivo:** Verificar los flujos principales de autenticación, carrito de compras y proceso de checkout.
* **Tipos de Testing:** Funcional, UI, Validaciones de campos y Negocio.
* **Entorno de Pruebas:** Google Chrome (Última versión) en Windows 11.

---

### 🐛 2. Reporte de Bugs Críticos Detectados

#### ❌ BUG 01: Error de autenticación con credenciales bloqueadas (UI/Funcional)
* **Descripción:** El sistema muestra un mensaje de error genérico en lugar de especificar que el usuario ha sido bloqueado por el administrador.
* **Pasos para reproducir:**
  1. Ir a `https://saucedemo.com`
  2. Introducir el usuario `locked_out_user`.
  3. Introducir contraseña válida `secret_sauce`.
  4. Hacer clic en "Login".
* **Resultado Esperado:** Mensaje informativo claro sobre el bloqueo de cuenta.
* **Resultado Actual:** El botón parpadea y muestra un error técnico no controlado.

#### ❌ BUG 02: Fallo de validación en el formulario de Checkout (UI)
* **Descripción:** El campo "Código Postal" permite avanzar en la compra introduciendo caracteres especiales y espacios en blanco, rompiendo la lógica del negocio.
* **Pasos para reproducir:**
  1. Añadir cualquier producto al carrito e iniciar Checkout.
  2. En el campo "Zip/Postal Code" escribir `#$% &*`.
  3. Hacer clic en "Continue".
* **Resultado Esperado:** Mensaje de error: "Código postal inválido".
* **Resultado Actual:** Permite continuar al último paso del pago.

---

### 📁 3. Evidencias y Logs
