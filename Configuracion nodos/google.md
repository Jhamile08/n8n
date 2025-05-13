# 🔐 Cómo configurar un nodo de Google en n8n

## ✅ Paso 1: Crear un proyecto en Google Cloud Console

1. Ve a [https://console.cloud.google.com/](https://console.cloud.google.com/).
2. Haz clic en el menú de la parte superior izquierda y selecciona  
   **"IAM y administración" → "Administrar recursos"**.
3. Crea un **nuevo proyecto** o selecciona uno existente.

---

## 🧩 Paso 2: Habilitar las APIs necesarias

1. Dentro del proyecto, ve a **"APIs y servicios" → "Biblioteca"**.
2. Busca y habilita las APIs que necesites. Ejemplos comunes:
   - **Google Sheets API**
   - **Gmail API**
   - **Google Drive API**

---

## 🛠️ Paso 3: Crear credenciales (Client ID y Client Secret)

1. Ve a **"APIs y servicios" → "Credenciales"**.
2. Haz clic en **"Crear credenciales"** → selecciona **ID de cliente de OAuth**.

3. Si te pide configurar la **pantalla de consentimiento OAuth**:
   - Tipo de usuario: selecciona **Externo**.
   - Completa el nombre de la app, correo del desarrollador y guarda.

4. Luego, crea el ID de cliente:
   - **Tipo de aplicación:** selecciona **Aplicación web**.
   - **Nombre:** puedes poner "n8n".
   - **URIs de redireccionamiento autorizados (Redirect URIs):**
     Agrega la URL que te da n8n en el nodo de Google, por ejemplo:

     ```
     http://localhost:5678/rest/oauth2-credential/callback
     ```

     > ⚠️ Si estás usando n8n en la nube o con dominio propio, reemplaza `localhost` por tu dominio.

5. Haz clic en **Crear**.
6. Copia el **Client ID** y el **Client Secret**.

---

## 🔁 Paso 4: Agregar credenciales en n8n

1. Abre tu panel de **n8n**.
2. Abre el nodo de Google que quieras usar (por ejemplo, Google Sheets).
3. En el campo de **credenciales**, haz clic en **"Crear nuevo"**.
4. Pega el **Client ID** y el **Client Secret** que obtuviste de Google Cloud.
5. Guarda y haz clic en **"Conectar cuenta"** para autenticarte con Google.

---

🎉 ¡Listo! Ya puedes usar nodos de Google en tus flujos de trabajo de n8n.
