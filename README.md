# 📌 n8n – Automatización de flujos de trabajo

## 🧠 ¿Qué es n8n?

**n8n** (pronunciado como "n-eight-n") es una herramienta de automatización de flujos de trabajo *open source* que permite conectar diferentes aplicaciones y servicios de forma visual y sin necesidad de escribir código complejo. Es una alternativa a herramientas como **Zapier** o **Make**, pero con más flexibilidad y capacidad de personalización.

Su nombre viene de "nodenodenode", haciendo referencia a los **nodos**, los bloques fundamentales de cada flujo.

---

## 🧱 ¿Qué son los nodos?

En **n8n**, un **nodo** es una unidad funcional que realiza una tarea específica. Cada nodo puede representar:

- Una aplicación o servicio externo (como Gmail, Slack, Trello, Google Sheets, etc.).
- Una operación lógica (como condicionales, bucles, filtros).
- Una transformación de datos (como formatear fechas, dividir texto, etc.).
- Funciones personalizadas en JavaScript.
- Acceso a bases de datos, APIs o archivos.

### Tipos comunes de nodos:

- **Trigger (disparador):** inicia el flujo.  
  Ej: al recibir un email, al llegar una petición HTTP, al actualizar una fila en Google Sheets.

- **Action (acción):** realiza una tarea.  
  Ej: enviar un mensaje, guardar datos, hacer una petición HTTP.

- **Function:** permite usar código JavaScript personalizado para manipular los datos.

---

## ⚙️ ¿Cómo funciona n8n?

El funcionamiento básico se puede describir en 3 pasos:

### 1. Creación del flujo:
- Se arrastran y conectan nodos en una interfaz gráfica (editor de flujos).
- Se configura cada nodo con la información necesaria (por ejemplo, qué mensaje enviar o a qué URL hacer una solicitud).

### 2. Ejecución del flujo:
- Puede ejecutarse automáticamente (por un trigger) o manualmente.
- Los datos fluyen de nodo en nodo, transformándose o accionando según se necesite.

### 3. Gestión de automatizaciones:
- Se puede programar la ejecución, definir condiciones, guardar historiales, y exportar/importar flujos.
- n8n se puede ejecutar en la nube, en local o en servidores propios (ideal para mantener el control de los datos).

---

## 🚀 Ejemplo rápido

Un flujo simple podría tener los siguientes nodos:

1. **Webhook Trigger**: espera una petición HTTP.  
2. **Set Node**: prepara o transforma los datos recibidos.  
3. **Gmail Node**: envía un correo electrónico con los datos.

---

## 🧩 Integraciones

n8n ofrece más de **300 integraciones** listas para usar, entre ellas:

- Google Drive  
- GitHub  
- Discord  
- Notion  
- Telegram  
- MySQL  
- PostgreSQL  
- ¡y muchas más!

---
