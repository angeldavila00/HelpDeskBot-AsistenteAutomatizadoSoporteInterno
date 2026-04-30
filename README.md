#  HelpDeskBot - Sistema de Automatización de Soporte

<p align="center">
  <img src="https://img.shields.io/badge/n8n-FF6D5A?style=for-the-badge&logo=n8n&logoColor=white" alt="n8n">
  <img src="https://img.shields.io/badge/Telegram-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  <img src="https://img.shields.io/badge/Google_Sheets-34A853?style=for-the-badge&logo=google-sheets&logoColor=white" alt="Google Sheets">
  <img src="https://img.shields.io/badge/status-funcional-brightgreen?style=for-the-badge" alt="Estado">
</p>

<p align="center">
  <strong>
HelpDeskBot es una solución de automatización de flujo de trabajo construida en n8n para gestionar tickets de soporte técnico de manera eficiente. El bot centraliza la comunicación a través de Telegram, procesa la información mediante lógica inteligente y mantiene un registro estructurado en Google Sheets para su seguimiento y resolución.
  </strong>
</p>

![!\[\]()](<img/Captura de pantalla 2026-04-29 200020.png>)

![alt text](<img/Captura de pantalla 2026-04-29 195245.png>)
![alt text](<img/Captura de pantalla 2026-04-29 195328.png>)
![alt text](<img/Captura de pantalla 2026-04-29 195546.png>)
![alt text](<img/Captura de pantalla 2026-04-29 195606.png>)
![alt text](<img/Captura de pantalla 2026-04-29 195653.png>)


---

##  Funcionalidades Principales

- **Recepción Multicanal:** Captura automática de mensajes y reportes desde un bot de Telegram.
- **Gestión de Estados:** Sistema lógico para identificar si un ticket es nuevo o requiere actualización de estado.
- **Integración con Hojas de Cálculo:** Lectura y escritura dinámica en Google Sheets para el control de inventario de tickets.
- **Procesamiento de Datos:** Uso de nodos de código JavaScript para transformar datos y personalizar las respuestas.
- **Notificaciones Automáticas:** Feedback inmediato al usuario sobre el estado de su requerimiento.

##  Estructura del Workflow (Nodos)

El archivo `.json` contiene la lógica estructurada de la siguiente manera:

- **Telegram Trigger:** Inicia el flujo cada vez que un usuario interactúa con el bot.
- **Switch/If Nodes:** Evalúan el contenido del mensaje y el estado actual del reporte.
- **Google Sheets Nodes:** - *Get row(s):* Consulta la base de datos existente.
    - *Update/Append:* Registra o modifica la información del ticket.
- **Code Nodes:** Ejecutan lógica personalizada en JavaScript para formatear la salida de los datos.
- **Telegram Send Message:** Envía confirmaciones y actualizaciones al usuario final.

##  Requisitos para la Implementación

1.  **n8n:** Tener una instancia activa (Local, Cloud o Docker).
2.  **Telegram Bot API:** Un token de bot generado a través de `@BotFather`.
3.  **Google Cloud Console:** Credenciales para la API de Google Sheets (OAuth2 o Service Account).
4.  **Hoja de Cálculo:** Un archivo de Google Sheets preparado con las columnas correspondientes (ID, Usuario, Mensaje, Estado).

##  Cómo Instalar el Workflow

1.  Copia el contenido del archivo `HelpDeskBot - Versión Final Conectada.json`.
2.  En tu instancia de **n8n**, crea un nuevo flujo de trabajo (Workflow).
3.  Pega el contenido directamente en el lienzo (canvas).
4.  Configura las credenciales:
    - Haz clic en el nodo de Telegram y añade tus credenciales.
    - Haz clic en los nodos de Google Sheets y conecta tu cuenta.
5.  Activa el flujo de trabajo mediante el interruptor **Active**.

## Autor

<div align="center">

**Proyecto de Automatización por Angel Niño Davila**

[![GitHub](https://img.shields.io/badge/GitHub-angeldavila00-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/angeldavila00)

</div>