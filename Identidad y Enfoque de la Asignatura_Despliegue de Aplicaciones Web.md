Este resumen de la asignatura **Despliegue de Aplicaciones Web**, impartida por el docente Damián, está diseñado para servir como contexto estructurado sobre los pilares, tecnologías y metodologías abordadas en el curso.

### **1. Identidad y Enfoque de la Asignatura**

La asignatura se centra en los "cimientos" para que una aplicación funcione fuera del entorno local, centrada en la **puesta en marcha y publicación de servicios web**. El enfoque es **eminentemente práctico y orientado al mundo real**, evitando el uso exclusivo de *localhost* y fomentando que los alumnos trabajen con sus propios **servidores VPS** y dominios contratados.

### **2. Infraestructura y Servidores Web (Apache y Nginx)**

El curso comienza con la administración de servidores, principalmente bajo **Linux (Ubuntu)**.

- **Modelo Cliente-Servidor:** Se explica mediante la analogía de un camarero (servidor) que responde a las peticiones (pedidos) del cliente.
- **Servidores Web:** Se trabaja extensamente con **Apache** (stack LAMP: Linux, Apache, MySQL, PHP) y se menciona **Nginx** como alternativa moderna.
- **Virtual Hosts:** Concepto clave que permite alojar múltiples sitios o subdominios en un mismo servidor y dirección IP mediante archivos de configuración en `sites-available`.
- **DNS (Domain Name System):** Gestión de registros (A, CNAME, MX, TXT) para apuntar dominios a IPs y entender la propagación global.

### **3. Despliegue de Aplicaciones Java (Tomcat)**

Una parte significativa se dedica al entorno de servidor para Java, utilizando **Apache Tomcat**.

- **Formatos de empaquetado:** Se diferencia entre el despliegue mediante archivos **WAR** (para servidores de aplicaciones como Tomcat que alojan múltiples apps) y archivos **JAR** (típicos de Spring Boot, que incluyen un servidor embebido y funcionan de forma "monolítica").
- **Servicios de Sistema:** Se enseña a configurar aplicaciones Java como **servicios de sistema** (`systemd`), permitiendo comandos como `systemctl start/stop` para gestionar la app en segundo plano.

### **4. Automatización y CI/CD (El "Estado del Arte")**

El núcleo avanzado de la asignatura es la **Integración Continua (CI) y el Despliegue Continuo (CD)**.

- **Filosofía:** Eliminar el error humano de las subidas manuales por FTP y pasar a un modelo donde un `git push` desencadena automáticamente la construcción, testeo y despliegue.
- **Herramientas:** Se utiliza **GitHub Actions** para crear **pipelines** (tuberías) que emulan entornos de construcción antes de enviar el artefacto final al servidor de producción (VPS o AWS).
- **Infraestructura como Código:** Uso de secretos en GitHub para manejar credenciales de forma segura sin exponerlas en el código.

### **5. Seguridad y Protocolos de Transferencia**

- **HTTPS y SSL/TLS:** Implementación de seguridad en la comunicación mediante **Let's Encrypt** y la herramienta **Certbot** para automatizar certificados gratuitos. Se explican conceptos de criptografía simétrica y asimétrica para entender el *handshake* del protocolo.
- **Transferencia de Archivos:** Aunque se enseña el uso de **FTP/SFTP** y programas como **FileZilla**, el curso evoluciona hacia métodos más seguros y automatizados como **SCP** a través de SSH.

### **6. Contenedores y Cloud Computing**

- **Docker:** Se introduce como la tendencia moderna para asegurar que el entorno de desarrollo sea idéntico al de producción, aunque se advierte de las limitaciones de recursos en VPS básicos.
- **Cloud (AWS):** Se realizan introducciones a servicios como **EC2** y se anima a los estudiantes a explorar la computación en la nube para obtener escalabilidad.

### **7. Objetivo Final**

El alumno debe ser capaz de realizar un **despliegue completo de una web** que incluya un *frontend* en **Angular** y un *backend* en **Spring Boot (API RESTful)** conectado a una base de datos **MariaDB/MySQL**, todo ello automatizado mediante un flujo de trabajo profesional.
