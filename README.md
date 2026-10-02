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
#### 🟢 BUG 01: LOW

* **Summary:** Button "Update" located on 'My cart' section doesn't highlight when there is an applicable update

* **Description:**
  * When the user write on the box below or modify the number of clothing items, th ebutton "Update" to apply the changes does not change to highlighted to notice the user that there are applicable changes and need to click to update
  
* **Steps:**
  1. Go to Sauce Demo home page
  2. Add something to cart
  3. Go to Check Out
  4. Change the quantity item value or write something on the box below
  5. See that the button "Update" are not changing to highligh when tthere is an applicable change
 
* **Actual Result:**
  * Button "Update" remains a dull gray when the user change some value
  
* **Expected Result:**
  * Button "Update" must switch to highlighted when the user change some value updatable

* **Environment:**
  * Browser: Brave / V
  * Versión: Brave 1.96.60 (Build oficial) (64 bits)
    Chromium: 154.0.8037.93
  * SO: WIndows 11 x64
    
* **Evidences:**
  * <img width="1691" height="1193" alt="BUG 01 LOW" src="https://github.com/user-attachments/assets/42829b56-e7a9-4263-8aba-773a613a44c1" />


#### 🟡 BUG 02: MEDIUM

* **Summary** The webpage keeps stucked in loading process when the user go to mycart after adding something

* **Description:**
  * If the user add something to cart, and from same spot, click on "My Cart" the webpage gets stucked in loading process without redirect to mycart section. The user need to refresh the webpage, go directly to checkout or change the way going to my cart to solve the problem for example going to another section and then clicking to mycart again to be redirected correctly
  
* **Steps:**
  1. Go to Sauce Demo home page
  2. Add something to cart
  3. Click on "My cart"
  4. See the result
 
* **Actual Result:**
  * Webpage gets stucked in loading process and doesn't redirect to my cart
  
* **Expected Result:**
  * Webpage should redirect the user to mycart without problem

* **Environment:**
  * Browser: Brave / V
  * Versión: Brave 1.96.60 (Build oficial) (64 bits)
    Chromium: 154.0.8037.93
  * SO: WIndows 11 x64
    
* **Evidences:**
   * <img width="1691" height="1193" alt="BUG 02 MEDIUM" src="https://github.com/user-attachments/assets/d262f2bb-f0f0-4c20-957a-bcc99af378a6" />


#### 🔴 BUG 03: CRITICAL

* **Summary:** The payment process fails due to a gateway failure

* **Description:**
  * There is a trouble with the payment process
  
* **Steps:**
  1. Having something on the cart go to check out section
  2. Click on check out to be redirected to payment process
  3. Fill the payment fields and click on "Pay Now"
  4. See the result
 
* **Actual Result:**
  * "There was an issue processing your payment. Try again or use a different payment method" mesage appears when the user try to perform the payment
  
* **Expected Result:**
  * The payment should be done correctly

* **Environment:**
  * Browser: Brave / V
  * Versión: Brave 1.96.60 (Build oficial) (64 bits)
    Chromium: 154.0.8037.93
  * SO: WIndows 11 x64
    
* **Evidences:**
  * <img width="1691" height="1193" alt="BUG 03 CRITICAL" src="https://github.com/user-attachments/assets/a7ced6d1-a3b0-41f9-a1b8-945a3c8f77ff" />


