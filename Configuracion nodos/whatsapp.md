# 💬 Cómo configurar WhatsApp en n8n usando la API de Meta (Facebook)

## ✅ Paso 1: Crear una cuenta de desarrollador en Meta

1. Ve a [https://developers.facebook.com/](https://developers.facebook.com/).
2. Iniciá sesión con tu cuenta de Facebook.
3. En el menú superior, hacé clic en **"Mis Apps"** → **"Crear App"**.
4. Tipo de aplicación: seleccioná **"Business"**.
5. Poné un nombre, email de contacto y creá la app.

---

## 📦 Paso 2: Configurar WhatsApp Business API

1. En el panel de tu app, andá a **"Agregar producto"**.
2. Buscá **WhatsApp** y hacé clic en **"Configurar"**.
3. Se creará una cuenta de prueba gratuita automáticamente.
4. Se te asignará un número de teléfono de prueba y un **Token de acceso temporal**.

---

## 🔐 Paso 3: Obtener credenciales

Anotá lo siguiente:

- **Token de acceso temporal** (luego deberás generar uno permanente).
- **ID del número de teléfono (Phone Number ID)**.
- **ID del negocio (Business Account ID)**.

Podés encontrarlos en la sección de configuración de WhatsApp → **"Getting Started"**.

---

## 🧪 Paso 4: Registrar un número de prueba

1. Agregá tu número de WhatsApp personal como receptor de prueba.
2. Enviá el código que te indica la plataforma para verificar el número.
3. Ya podés enviar mensajes desde tu número de prueba a ese número.

---

## ⚙️ Paso 5: Crear las credenciales en n8n

1. En n8n, creá una **credencial HTTP Request**:
   - Tipo: **HTTP Request**.
   - Nombre: "WhatsApp Meta API".
   - **Authentication**: Bearer Token.
   - **Token**: Pegá tu Token de acceso temporal (o permanente si ya lo generaste).
   - Guardá.

---

## 🛠️ Paso 6: Configurar el nodo HTTP Request

1. Añadí un nodo `HTTP Request` en tu flujo.
2. Configurá los siguientes campos:

   - **HTTP Method**: `POST`
   - **URL**:  
     ```
     https://graph.facebook.com/v19.0/<PHONE_NUMBER_ID>/messages
     ```
     Reemplazá `<PHONE_NUMBER_ID>` por el tuyo real.

   - **Authentication**: Seleccioná la credencial creada anteriormente.

   - **Headers**:
     ```json
     {
       "Content-Type": "application/json"
     }
     ```

   - **Body Parameters (RAW → JSON)**:
     ```json
     {
       "messaging_product": "whatsapp",
       "to": "5491123456789",
       "type": "text",
       "text": {
         "body": "¡Hola desde n8n usando la API de Meta!"
       }
     }
     ```

3. Ejecutá el nodo. Si todo está bien configurado, recibirás el mensaje en tu WhatsApp.

---

## 🧩 Recomendaciones

- El **token temporal** vence cada 24 horas. Para producción, deberás configurar el **token permanente con OAuth**.
- Si querés usar tu número real de empresa, deberás verificar tu cuenta y registrar el número en el [Centro de empresas](https://business.facebook.com/).

---

🎉 ¡Listo! Ahora tenés WhatsApp Business Cloud API funcionando con n8n usando la API oficial de Meta.
