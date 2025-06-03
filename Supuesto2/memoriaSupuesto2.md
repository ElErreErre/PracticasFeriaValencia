# RETO FERIA VALENCIA  
## SUPUESTO 2

**Rubén Ramírez Cataluña – 1ºDAM**

---

## ÍNDICE

- [ANÁLISIS Y PLANIFICACIÓN](#análisis-y-planificación)  
- [DISEÑO](#diseño)  
- [TEST CON USUARIOS](#test-con-usuarios)  
- [DESARROLLO Y ENVÍO DE CORREOS](#desarrollo-y-envío-de-correos)  
- [INTEGRACIÓN CON REDES SOCIALES](#integración-con-redes-sociales)  
- [CONTROL DE VERSIONES CON GITHUB](#control-de-versiones-con-github)  
- [PERSONALIZACIÓN DEL CORREO MJML](#personalización-del-correo-mjml)  
- [VERIFICAR COMPATIBILIDAD CON DIFERENTES CLIENTES DE CORREO](#verificar-compatibilidad-con-diferentes-clientes-de-correo)  
- [DOCUMENTACIÓN FINAL](#documentación-final)

---

## ANÁLISIS Y PLANIFICACIÓN

### Análisis de requerimientos

**Público Objetivo Principal:**  
Expositores actuales y potenciales de Cevisama, empresas del sector cerámico, equipamiento de baño, piedra natural, tecnología, etc.

**Subsegmentos:**  
- Expositores de ediciones anteriores.  
- Expositores con poca o nula experiencia en exportación.

### DAFO y competencia

**Fortalezas:**  
- Marca ferial reconocida.  
- Inversión en atracción de compradores internacionales.

**Debilidades:**  
- Percepción de enfoque nacional.  
- Falta de concreción en beneficios.

**Oportunidades:**  
- Creciente necesidad de internacionalización.  
- Posicionarse como feria clave en España para compradores internacionales.

**Amenazas:**  
- Competencia internacional como Cersaie.  
- Fluctuaciones económicas/políticas.

### Objetivo de la campaña

Aumentar reservas de espacio y confirmaciones de participación mediante una campaña de email marketing directa y persuasiva.

---

## DISEÑO

### Mockup

Mockup realizado con **Figma**, centrado en cabecera y footer, el resto con bloques de imagen y *Lorem Ipsum*.  
**[Imagen Placeholder]**

### Responsive avanzado con MJML

MJML es responsive por defecto.  
Se aplicó una *media query* a un botón por errores de visualización específicos.

---

## TEST CON USUARIOS

**Selección de muestra:**  
Alumnos, profesores y amigos han participado dando feedback.  

Se utilizó un formulario de **Google Forms** con una escala de 1 a 5 sobre diferentes aspectos de la newsletter.

---

## DESARROLLO Y ENVÍO DE CORREOS

**Tecnologías usadas:**  
- **AWS EC2**  
- **Node.js**  
- **MySQL**  
- **MJML**  
- **Nodemailer**

**Pasos realizados:**

1. Configuración de instancia EC2 (Ubuntu).
2. Conexión por SSH.
3. Instalación de MySQL, creación de base de datos y usuario.
4. Instalación de Node.js y dependencias:
   - `nodemailer`
   - `mysql2`
   - `mjml`
5. Estructura del proyecto con `app.js` y `emailService.js`.
6. Uso de `.env` para credenciales y configuración sensible.
7. Pruebas iniciales en cuentas de Gmail y Outlook.

**Nota:** Los correos llegan a spam por defecto. Es necesario marcar como seguro para ver correctamente imágenes.

**Repositorio:**  
[GitHub - PracticasFeriaValencia](https://github.com/ElErreErre/PracticasFeriaValencia)

---

## INTEGRACIÓN CON REDES SOCIALES

### Enfoque inicial descartado:
- Creación de videos explicativos (poca eficacia por público objetivo específico).

### Solución aplicada:
- **Campañas publicitarias** en formato vertical (TikTok, Instagram Reels).
- Segmentación directa, sin depender del algoritmo.

---

## CONTROL DE VERSIONES CON GITHUB

Uso de **GitHub** con Visual Studio Code.  
Commits regulares realizados según avances.  
El primer commit corresponde a una primera versión funcional. Los siguientes reflejan mejoras tras feedback recibido.

Repositorio:  
[https://github.com/ElErreErre/PracticasFeriaValencia](https://github.com/ElErreErre/PracticasFeriaValencia)

---

## PERSONALIZACIÓN DEL CORREO MJML

Se personaliza el **asunto** y el **contenido** con parámetros como `{nombre}` extraídos de la base de datos.  
Esto se hace mediante *strings* personalizados dentro del archivo `app.js`.

---

## VERIFICAR COMPATIBILIDAD CON DIFERENTES CLIENTES DE CORREO

Verificación en **Gmail** y **Outlook**.  
Se han evitado características no compatibles (como GIFs o carruseles) para asegurar visualización completa.

---

## DOCUMENTACIÓN FINAL

### Guía de usuario

1. **Abre tu Newsletter:**  
   Busca el correo de Cevisama. Revisa spam si no lo encuentras.
2. **Lee la Información de la Feria:**  
   Detalles sobre beneficios para expositores.
3. **Haz clic en “Más información”:**  
   Acceso a más detalles desde la newsletter.

### Informe final del proyecto

Este proyecto busca dar a conocer **Cevisama** a expositores nuevos y recurrentes.  
Además de newsletter, se ha apostado por **publicidad en redes sociales** para ampliar el alcance.  

En el diseño, se ha optado por un enfoque **minimalista** en bloques para facilitar la lectura.  

El mayor reto ha sido la automatización del envío de correos con Node.js y MJML.  

El feedback recibido ha permitido pulir los detalles finales y mejorar la calidad global del proyecto.

---
