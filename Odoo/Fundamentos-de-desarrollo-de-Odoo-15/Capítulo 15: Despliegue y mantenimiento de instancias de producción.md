## Capítulo 15: Despliegue y mantenimiento de instancias de producción
En este capítulo, aprenderás los conceptos básicos de la preparación de un servidor Odoo para su uso en un entorno de producción.

La configuración y el mantenimiento de servidores es un tema no trivial en sí mismo y debe ser realizado por especialistas. La información que aquí se ofrece no es suficiente para garantizar que un usuario medio pueda crear un entorno resistente y seguro que aloje datos y servicios sensibles.

El objetivo de este capítulo es introducir los aspectos de configuración más importantes y las mejores prácticas específicas para los despliegues de Odoo. Esto ayudará a los administradores de sistemas a preparar sus hosts de servidores Odoo.

Empezarás configurando el sistema anfitrión, y luego instalarás los prer-requisitos de Odoo y el propio Odoo. Ubuntu es una elección popular para servidores en la nube, y será usado aquí. Luego, el archivo de configuración de Odoo necesita ser preparado. Hasta este punto, la configuración es similar a la utilizada para el entorno de desarrollo.

A continuación, Odoo necesita ser configurado como un servicio del sistema para que se inicie automáticamente cuando se inicie el servidor.

Para servidores alojados en una nube pública, Odoo debe ser servido a través de HTTPS. Para esto, aprenderás como instalar y configurar un proxy inverso Nginx usando un certificado autofirmado.

En la última sección se explica cómo realizar actualizaciones de servidores y preparar un entorno de ensayo que nos permita realizar pruebas de funcionamiento antes de aplicar las actualizaciones reales.

Los temas tratados en este capítulo son los siguientes:
* Preparación del sistema anfitrión
* Instalar Odoo desde el código fuente
* Configurando Odoo
* Configurar Odoo como un servicio del sistema
* Configurando un proxy inverso Nginx
* Configurando y reforzando HTTPS
* Manteniendo el servicio y los módulos de Odoo

Al final de este capítulo, serás capaz de configurar un servidor Odoo razonablemente seguro que sea lo suficientemente bueno para un uso de producción de bajo perfil. Sin embargo, las recetas dadas en este capítulo no son la única forma válida de desplegar Odoo - otros enfoques también son posibles.

---
### Requisitos técnicos
Para seguir este capítulo, necesitarás un servidor Ubuntu 20.04 limpio - por ejemplo, un servidor virtual privado (VPS) alojado en la nube.

El código y los scripts utilizados en este capítulo se encuentran en el directorio `ch15`/ del repositorio de GitHub en (https://github.com/PacktPublishing/Odoo-15-Development-Essentials)[https://github.com/PacktPublishing/Odoo-15-Development-Essentials].
