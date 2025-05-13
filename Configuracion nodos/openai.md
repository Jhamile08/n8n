# 🤖 Cómo configurar un nodo de OpenAI en n8n

## ✅ Paso 1: Crear una cuenta en OpenAI

1. Ve a [https://platform.openai.com/](https://platform.openai.com/).
2. Si no tenés una cuenta, registrate con tu correo.
3. Iniciá sesión en el panel de OpenAI.

---

## 🔐 Paso 2: Obtener tu API Key

1. En la parte superior derecha, hacé clic en tu nombre o ícono de perfil.
2. Seleccioná **"View API Keys"**.
3. Hacé clic en **"Create new secret key"**.
4. Copiá y guardá la **API Key**. ⚠️ No podrás verla de nuevo más adelante.

---

## 🛠️ Paso 3: Agregar la API Key en n8n

1. Abrí tu panel de **n8n**.
2. Añadí un nodo de OpenAI (por ejemplo, `OpenAI`, `ChatGPT`, `Text-Davinci`, etc.).
3. En el campo de **credenciales**, hacé clic en **"Crear nuevo"**.
4. Pegá tu **API Key** en el campo correspondiente.
5. Asigná un nombre a tus credenciales y guardá.

---

## ✨ Paso 4: Usar el nodo

1. Elegí el modelo que querés usar, por ejemplo:
   - `gpt-3.5-turbo`
   - `gpt-4`
   - `text-davinci-003` (modelos legacy)
2. Ingresá tu prompt o configuración deseada.
3. Conectalo con otros nodos si querés automatizar respuestas, procesar datos, enviar por email, etc.
4. Ejecutá el flujo.

---

🎉 ¡Listo! Ahora podés usar la potencia de OpenAI en tus flujos de trabajo automatizados con n8n.
