# Muestra: flujo "Pedidos Email a PDF"

Exportación del flujo en producción, lista para importar en n8n (**Import from File**). Se han quitado los identificadores de credenciales, el buzón, el chat de Telegram, la dirección de la base de datos y los recursos embebidos (logo y fuentes en base64).

Lo más interesante para revisar está en dos nodos de código:

- **Extraer pedido + preparar HTML**: lee el correo en crudo (MIME), saca el número de pedido del asunto o del cuerpo, clasifica el pedido (chapa, cristal o mixto) e incrusta en la ficha las imágenes del correo.
- **Construir index.html**: plantilla A4 de la ficha que Gotenberg convierte a PDF.

Para usarlo hay que crear las credenciales de Gmail, Google Drive, Telegram y la base de datos, y sustituir `TELEGRAM_CHAT_ID`, `TU-PROYECTO` y `USUARIO_SISTEMA_UID`.
