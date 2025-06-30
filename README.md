# Chat WebSocket con NestJS

---

## Descripción

Este proyecto es un ejemplo básico de un servidor WebSocket implementado con **NestJS** que permite la comunicación en tiempo real entre múltiples clientes. Los clientes pueden enviar mensajes de chat que se retransmiten a todos los usuarios conectados.

---

## Tecnologías usadas

- **NestJS**: Framework backend para Node.js.
- **Socket.IO**: Librería para WebSockets que facilita comunicación bidireccional.
- **Prisma** (opcional): ORM para manejar persistencia en base de datos (no implementado aún).
- **TypeScript**: Lenguaje principal del proyecto.

---

## Instalación

1. Clona el repositorio:
   ```bash
   git clone <https://github.com/CarlosArgudo1D/websocket.git>
   cd <websocket>

## Instalación de dependencias y ejecución del servidor

Instala las dependencias compatibles con NestJS 10:

```bash
npm install
npm install --save @nestjs/websockets@10.0.10 @nestjs/platform-socket.io@10.0.10

## Inicia el servidor NestJS

```bash
npm run start


Funcionamiento
El servidor WebSocket está disponible en el puerto 3000.

Permite conexiones desde cualquier origen (CORS configurado con origin: '*').

Los clientes pueden conectarse y enviar mensajes con el evento "chatMessage".

Cuando el servidor recibe un mensaje, lo imprime en consola y lo reenvía a todos los clientes conectados (broadcast).


> El archivo HTML de prueba (`client.html`) se encuentra incluido en el mismo proyecto, en la carpeta `html/` (o en la raíz del proyecto)

## Abrir el cliente HTML existente

Una vez clonado el proyecto y con el servidor corriendo (`npm run start:dev`):

1. En tu explorador de archivos, navega hasta la carpeta `html` que ya está en el repositorio.
2. Haz **doble clic** sobre `client.html`.
3. El navegador predeterminado abrirá la página y establecerá la conexión WebSocket automáticamente con `http://localhost:3000`.
4. Para verificarlo, abre la consola de desarrollador (F12) y busca el mensaje de “Conectado al servidor WebSocket”.  
5. Envía un mensaje y comprueba que aparece en la lista en tiempo real. Puedes repetir en otra pestaña para ver el broadcast.  

