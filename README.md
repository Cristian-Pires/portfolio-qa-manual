# 🛠️ Mi Proyecto de QA Manual - Auditoría de Pruebas

Este es mi repositorio personal de QA Manual. Aquí documento las pruebas de caja negra realizadas en entornos web de prueba, clasificando los hallazgos por niveles de severidad para el negocio.

---

### 📊 Datos del Entorno
* **Sitio Web Auditado:** https://sauce-demo.myshopify.com/
* **Navegador:** Brave / Versión: Brave 1.96.60 (Build oficial) (64 bits)
                                  Chromium: 154.0.8037.93
* **Sistema Operativo:** Windows 11

---

### 🐛 Historial de Bugs Reportados

* **Summary** Button "Updaste" located on 'My cart' section doesn't highlight when there is an applicable update

* **Description:**
  * When the user write on the box below or modify the number of clothing items, th ebutton "Update" to apply the changes does not change to highlighted to notice the user that there are applicable changes and need to click to update
  
* **Steps:**
  1. Go to Sauce Demo home page
  2. Add something to cart
  3. Go to Check Out
  4. Change Quantity value or write something on the box below
  5. See that the button "Update" are not changing to highligh when tthere is an applicable change
 
* **Actual Restul:**
* Button "Update" remains a dull gray when the user change some value
  
* **Expected Result:**
* Button "Update" must switch to highlighted when the user change some value updatable

* **Environment**
* Browser: Brave / V
* Versión: Brave 1.96.60 (Build oficial) (64 bits)
  Chromium: 154.0.8037.93
