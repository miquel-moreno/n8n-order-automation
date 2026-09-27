# n8n Order Automation

Lleva cada pedido de un taller de chapa **del correo del cliente al taller** sin escribir nada a mano. En producción.

> Flujo exportado, sin datos sensibles, en [`sample/`](sample/).

![Flujo de pedidos: del correo al PDF](./images/n8n-pedidos-email-pdf.png)

## Cómo funciona

1. Llega un correo de pedido de un remitente autorizado.
2. n8n extrae el número de pedido y los planos, genera la **ficha en PDF** y la guarda en Google Drive.
3. Registra el pedido en el [panel del taller](https://github.com/miquel-moreno/workshop-order-management) y avisa por **Telegram**.
4. Cuando el pedido se termina, genera la **etiqueta en PDF** y la envía.

## Stack

n8n autoalojado · Gmail · Google Drive · Telegram · API REST · Gotenberg (HTML → PDF) · Docker

## Mi papel

Análisis del proceso con el taller, diseño de los flujos y las plantillas, puesta en producción y mantenimiento.

---

[Perfil](https://github.com/miquel-moreno) · [LinkedIn](https://www.linkedin.com/in/miquel-moreno-martinez)