El examen del segundo trimestre de la asignatura **Despliegue de Aplicaciones Web** consiste en una **prueba eminentemente práctica** centrada en la automatización profesional del despliegue. A continuación, se detallan las instrucciones precisas extraídas de las fuentes:

### **Información General y Objetivos**

- **Contenido principal:** Deberás realizar el **despliegue automático de una web completa**.
- **Enfoque:** El objetivo no es evaluar tus habilidades de desarrollo *frontend*, sino el **proceso de despliegue automatizado**.
- **Duración:** Dispondrás de **hora y media** para completar la prueba (aunque si se ha practicado, puede resolverse en unos 20 minutos).

### **Requisitos Técnicos y Herramientas**

Para realizar el examen será necesario utilizar y configurar las siguientes herramientas:

- **Framework:** Una aplicación desarrollada en **Angular**.
- **Control de Versiones:** Uso obligatorio de un repositorio **Git** completo (preferiblemente en GitHub).
- **Automatización (CI/CD):** Configuración de un **pipeline completo** funcional (GitHub Actions) que ejecute el despliegue al realizar un *push*.
- **Servidor y Sistema:** Un servidor **VPS** (habitualmente Ubuntu) con **Apache** configurado.
- **Gestión de Red:** Deberás configurar el **DNS** para que apunte al servidor y crear un **Virtual Host** específico que apunte a la ruta de la aplicación.

### **Lo que está Prohibido o Excluido**

- **LDAP:** El docente ha confirmado explícitamente que el tema de **LDAP está quitado del examen** y de las prácticas, por ser un tema más orientado a sistemas que al despliegue web propiamente dicho.
- **Intervención Manual:** El despliegue debe ser automático; no se valorará positivamente el uso de métodos manuales como subir archivos por FTP para la entrega final.

### **Formato de Entrega**

La entrega debe ser completa para ser evaluada y debe incluir:

1. **Repositorio:** El enlace al código fuente que incluya el archivo de **workflow de GitHub Actions** perfectamente funcional.
2. **Documento PDF:** Un informe que contenga:
   - Capturas de pantalla del repositorio en GitHub.
   - Capturas del **workflow** (pipeline) funcionando correctamente.
   - Capturas del navegador mostrando la aplicación cargada desde la IP o dominio del **VPS**.
   - Una breve **explicación** de lo que has implementado.

Se recomienda haber practicado previamente la vinculación entre el repositorio y el VPS mediante **secretos (Secrets)** de GitHub para asegurar que el pipeline no falle durante la prueba. Si lo deseas, puedo crear un **cuestionario de repaso** o una **guía de pasos** basada en las fuentes para que practiques el flujo del examen.
