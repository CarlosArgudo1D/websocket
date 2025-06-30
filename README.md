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
   git clone <url-del-repositorio>
   cd <nombre-del-proyecto>

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



