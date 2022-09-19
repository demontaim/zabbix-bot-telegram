# Bot de Telegram para Servidores Zabbix

Documentación sobre como implementar un bot de Telegram en un servidor Zabbix.

---

## Requisitos

* Servidor Zabbix 3.0 o superior
* Canal de Telegram
* Bot de Telegram

## ¿Para qué sirve un servidor Zabbix?

Zabbix es una herramienta de monitoreo de red y aplicaciones, que permite monitorear la disponibilidad y el rendimiento de sus servidores, aplicaciones y redes. Zabbix es una herramienta de código abierto, lo que significa que es gratuita y que puede ser modificada para adaptarse a sus necesidades.

## ¿Para qué sirve un bot de Telegram?

Un bot de Telegram es un programa que se ejecuta dentro de Telegram. Puede realizar tareas como buscar información en Internet, descargar archivos, enviar mensajes, etc. Los bots de Telegram son una forma divertida de interactuar con sus amigos o simplemente pasar el rato.

## ¿Para qué sirve un canal de Telegram?

Un canal de Telegram es un tipo de chat que puede tener un número ilimitado de miembros. Los canales son una forma de comunicarse con sus clientes o suscriptores. Puede enviar mensajes, archivos, fotos, videos, etc. a todos sus miembros de una sola vez.

## ¿Cómo funciona?

El bot de Telegram se comunica con el servidor Zabbix a través de la API de Zabbix. El bot de Telegram se comunica con el canal de Telegram a través de la API de Telegram. Se reciben alertas de los servidores Zabbix y se envían a los canales de Telegram.

---

## Guía paso a paso

### 1. Crear un bot de Telegram

Para crear un bot de Telegram, debe iniciar sesión en Telegram y buscar el bot @BotFather. Luego, envíe el comando /newbot y siga las instrucciones.

```console

demontaim@heaven:~$ /newbot

```

Después de crear el bot, otorgarle una descripción y nombre, el BotFather le dará un token de acceso. Guarde este token de acceso, ya que lo necesitará más adelante.

### 2. Crear un canal de Telegram

Creamos un canal de Telegram e invitamos al bot de Telegram como si de un usuario normal se tratara.

A su vez también añadimos al bot RawDataBot, que nos permitirá obtener el ID del canal.

Una vez que tenemos a los dos bots en el grupo escribimos /getgroupid y automáticamente nos devolverá el ID de la sección Chat que usaremos con el Token para configurar Zabbix.

```console

demontaim@heaven:~$ /getgroupid

```
