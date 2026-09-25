# TMI n8n Automations · Automatización de pedidos

Flujos de n8n de TMI System (Tenkai Global) que llevan cada pedido desde el correo del cliente hasta el taller, sin registro manual. Dos flujos en producción.

> Los flujos no se publican: contienen identificadores de las cuentas conectadas. Aquí se explica qué hacen y cómo están montados.

<!-- CAPTURAS: el lienzo de n8n de cada flujo, sin datos de clientes ni direcciones
![Flujo de entrada de pedidos](./images/flujo-pedidos.png)
![Ficha de pedido generada](./images/ficha-pedido.png)
-->

## Qué resuelve

Los pedidos llegaban por correo y se pasaban a mano: copiar datos, crear la ficha, guardarla y avisar al taller. Era lento y fácil equivocarse.

## Cómo funciona

```
Correo con el pedido
      ↓
n8n lee el correo y extrae los datos
      ↓
Genera la ficha del pedido en PDF
      ↓
La guarda en Google Drive
      ↓
Avisa al taller por Telegram
      ↓
El taller confirma cuando el trabajo está terminado
```

## Qué hace

- **Entrada automática de pedidos** desde el correo.
- **Ficha de pedido en PDF** con plantilla propia de la empresa.
- **Archivo ordenado** en Google Drive.
- **Aviso al taller por Telegram** y confirmación de trabajo terminado.

## Cómo está hecho

| | |
|---|---|
| **Automatización** | n8n |
| **Integraciones** | Correo electrónico · Google Drive · Telegram |
| **Plantillas** | HTML a PDF |
| **Infraestructura** | n8n autoalojado en servidor propio |

- **Credenciales guardadas en n8n**, nunca dentro de los flujos.

## Mi papel

Análisis del proceso con el taller, diseño de los flujos y las plantillas, puesta en producción y mantenimiento.

---

[Perfil](https://github.com/miquel-moreno) · [LinkedIn](https://www.linkedin.com/in/miquel-moreno-martinez)
