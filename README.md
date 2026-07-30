# ☕ DeliveryBot

Bot de Telegram desarrollado en **n8n** para automatizar pedidos de una cafetería utilizando **Google Sheets** como base de datos.

---

## 🚀 Características

- Menú interactivo desde Telegram
- Categorías dinámicas
- Visualización de productos
- Carrito de compras
- Confirmación de pedidos
- Historial de pedidos
- Seguimiento de pedidos
- Notificaciones automáticas a cocina
- Gestión de sesiones de usuarios
- Base de datos en Google Sheets

---

## 🛠 Tecnologías

- n8n
- Telegram Bot API
- Google Sheets
- JavaScript
- HTTP Request

---

## 📂 Base de Datos

El proyecto utiliza un archivo de Google Sheets con varias hojas.

### MENU

Contiene todos los productos.

| Campo | Descripción |
|--------|-------------|
| id_producto | ID del producto |
| nombre | Nombre |
| categoria | Categoría |
| descripcion | Descripción |
| precio | Precio |
| stock | Inventario |

---

### SESSIONS

Guarda la sesión de cada usuario.

| Campo |
|--------|
| telegram_id |
| pantalla_actual |
| carrito_temporal |
| categoria_seleccionada |
| ultimo_producto_visto |
| nota_temporal |
| ultimo_cambio |

---
### USUARIO

Guarda la sesión de cada usuario.

| Campo |
|--------|
| telegram_id |
| nombre_completo |
| fecha_-registro |
| ultimo_pedido |

---

### PEDIDO

Guarda la sesión de cada usuario.

| Campo |
|--------|
| id_pedido |
| telegram_id |
| nombre_usuario |
| detalles_pedido |
| total_pago |
| ESTADO |
| fecha |
| hora |

---
## 📱 Flujo del Bot

```
Usuario
    │
    ▼
Telegram
    │
    ▼
Telegram Trigger
    │
    ▼
Normalizar Entrada
    │
    ▼
Obtener Sesión
    │
    ▼
Procesar Acción
    │
    ▼
Construir Mensaje
    │
    ▼
Enviar Respuesta
```

---

## 📦 Flujo de Compra

```
Inicio

↓

Ver menú

↓

Seleccionar categoría

↓

Seleccionar producto

↓

Ver detalle

↓

Agregar al carrito

↓

Seleccionar cantidad

↓

Confirmar pedido

↓

Guardar pedido

↓

Notificar cocina

↓

Confirmación al cliente
```

---

## ⚙️ Funciones

- Inicio del bot
- Menú dinámico
- Categorías
- Productos
- Detalle del producto
- Carrito
- Confirmación
- Historial
- Seguimiento
- Ayuda

---

## 📋 Principales nodos

| Nodo | Función |
|------|---------|
| Telegram Trigger | Recibe mensajes |
| Normalizar Entrada | Procesa la información recibida |
| Obtener Sesión | Consulta Google Sheets |
| Procesar Interacción | Determina la acción del usuario |
| Actualizar Sesión | Guarda cambios |
| Construir Mensaje | Genera el mensaje dinámico |
| Cargar Categorías | Obtiene categorías |
| Cargar Productos | Obtiene productos |
| Detalle Producto | Muestra información |
| Confirmar Pedido | Procesa el pedido |
| HTTP Cocina | Envía el pedido |
| Telegram | Envía respuesta al usuario |

---

## 📋 Requisitos

- n8n
- Cuenta de Telegram
- BotFather
- Google Cloud
- Google Sheets API

---

## 🔧 Instalación

1. Clonar el repositorio

```bash
git clone https://github.com/tuusuario/DeliveryBot.git
```

2. Importar el workflow en n8n.

3. Crear el bot en Telegram con BotFather.

4. Configurar las credenciales de Telegram.

5. Configurar Google Sheets OAuth.

6. Actualizar los IDs de las hojas.

7. Activar el workflow.

---

## 📂 Estructura

```
DeliveryBot/

│
├── README.md
├── workflow.json

```

---

## 📌 Funcionalidades

✅ Registro automático de usuarios

✅ Sesiones persistentes

✅ Carrito temporal

✅ Productos dinámicos

✅ Categorías dinámicas

✅ Confirmación de pedido

✅ Historial

✅ Seguimiento

✅ Notificación a cocina

---

## 🔄 Flujo general

```
Telegram

↓

Webhook

↓

Procesar mensaje

↓

Consultar sesión

↓

Consultar productos

↓

Construir respuesta

↓

Enviar mensaje

↓

Actualizar sesión
```

---

## 📸 Capturas

## Menú Principal

![Menú](telegram.png)

## Agregar al carrito

![Carrito](telegram1.png)

## Confirmación

![Confirmación](telegram2.png)

## Historial

![Historial](telegram3.png)

## Seguimiento

![Seguimiento](telegram4.png)


---

## 🚀 Mejoras futuras

- Pagos en línea
- Integración con WhatsApp
- Base de datos MySQL
- Panel administrativo
- Dashboard
- Inventario automático
- Estadísticas
- IA para recomendaciones

---

## 👨‍💻 Autor

Desarrollado por **Maria Jose ANGULO**

Proyecto académico desarrollado en **n8n** utilizando Telegram y Google Sheets.

---

## 📄 Licencia

Este proyecto es de uso académico y puede modificarse libremente para fines educativos.

---
