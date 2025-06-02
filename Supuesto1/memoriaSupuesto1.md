# RETO FERIA VALENCIA

## SUPUESTO 1

**Rubén Ramírez Cataluña - 1ºDAM**

---

## ÍNDICE

- ANÁLISIS Y PLANIFICACIÓN
- DISEÑO
- TEST CON USUARIOS
- DESARROLLO Y ENVÍO DE CORREOS
- INTEGRACIÓN CON REDES SOCIALES
- CONTROL DE VERSIONES CON GITHUB
- PERSONALIZACIÓN DEL CORREO MJML
- VERIFICAR COMPATIBILIDAD CON DIFERENTES CLIENTES DE CORREO
- DOCUMENTACIÓN FINAL

---

## ANÁLISIS Y PLANIFICACIÓN

### Análisis de requerimientos

El Salón del Cómic de València atrae a una diversidad de públicos, cada uno con intereses y necesidades distintas. Identificar estos segmentos nos permitirá adaptar el contenido y el tono del boletín para maximizar su impacto:

**Visitantes (Público General):**

- Aficionados al cómic, manga, anime y cultura pop.
- Familias con niños.
- Compradores y coleccionistas.

La newsletter debe ser concisa y directa al grano. El público general es joven, interesado en cómics, manga, artistas influyentes, videojuegos, cosplay y cultura pop.

### DAFO y competencia

**Fortalezas:**

- **Posicionamiento Reconocido:** trayectoria y prestigio en València.
- **Oferta Temática Amplia:** cómic, manga, anime, videojuegos, cosplay.

**Debilidades:**

- **Interés Estacionalizado:** atención concentrada en fechas cercanas al evento.
- **Dependencia de Asistencia Física:** vulnerable a factores externos.

**Oportunidades:**

- **Mercado en Expansión:** creciente interés en la temática.
- **Alianzas Estratégicas:** colaboración con empresas e instituciones.
- **Nuevas Tecnologías:** uso de VR/AR, streaming, contenido digital.

**Amenazas:**

- **Fuerte Competencia:** otros eventos similares en España.
- **Contexto Económico Variable:** crisis o inflación.

### Objetivo de la campaña

Incrementar la asistencia y el engagement entre el público joven (15-35 años) y aumentar la venta anticipada de entradas en un 15% mediante una comunicación digital atractiva a través del boletín.

---

## DISEÑO

### Mockup

Creado con **Figma**. Se definió la cabecera y el footer, el resto está en prototipado con imágenes de ejemplo y texto *Lorem Ipsum*.

### Responsive avanzado con MJML

MJML es responsive por defecto. Se aplicó una *media query* a un botón que no funcionaba correctamente. Por lo demás, el sistema se comporta adecuadamente.

---

## TEST CON USUARIOS

### Selección de muestra

Participaron alumnos, profesores y amigos, quienes aportaron feedback objetivo. Se usó un **Google Forms** con puntuaciones del 1 al 5.

Aún no se ha hecho un rediseño, pero se sigue aceptando feedback constructivo.

---

## DESARROLLO Y ENVÍO DE CORREOS

### Tecnología utilizada

- **AWS EC2** para montar un servidor Ubuntu.
- **MySQL** para almacenar usuarios (nombre, correo y ciudad).
- **Node.js** con las librerías:
  - `nodemailer` (envío de correos)
  - `mysql2` (conexión a MySQL)
  - `mjml` (plantillas de correo)
- **Archivo .env** con credenciales (SMTP, DB, etc.).

### Funcionamiento

`app.js` gestiona la conexión a la base de datos, compila la plantilla `newsletter.mjml` y usa `emailService.js` para enviar los correos de forma personalizada.

**Pruebas realizadas:** Con cuentas de Gmail y Outlook. Los correos llegan a la carpeta de spam, lo que impide la carga automática de imágenes hasta marcar como seguro.

**Más información:** consultar el documento **AWS NODE.JS** en el [repositorio de GitHub](https://github.com/ElErreErre/PracticasFeriaValencia).

---

## INTEGRACIÓN CON REDES SOCIALES

Se eligió **TikTok** por su capacidad de viralización y facilidad de difusión sin búsqueda previa.

El contenido se reutiliza en **Instagram Reels** y **YouTube Shorts**, cubriendo así las principales redes actuales de contenido vertical.

---

## CONTROL DE VERSIONES CON GITHUB

Repositorio: [https://github.com/ElErreErre/PracticasFeriaValencia](https://github.com/ElErreErre/PracticasFeriaValencia)

- Uso de la integración de Git en **Visual Studio Code**.
- Commits frecuentes, especialmente tras cada avance o feedback recibido.
- El primer commit suele marcar el final de una primera versión, seguido de mejoras sucesivas.

---

## PERSONALIZACIÓN DEL CORREO MJML

El primer envío solo incluía la plantilla MJML. Se investigó cómo añadir contenido dinámico y personalizado con parámetros como `{nombre}` en el mensaje.

Esto se define en `app.js`, personalizando el asunto y el cuerpo del mensaje con datos extraídos desde la base de datos.

---

## VERIFICAR COMPATIBILIDAD CON DIFERENTES CLIENTES DE CORREO

Se realizaron pruebas en **Gmail** y **Outlook**.

Se evitaron funciones de MJML incompatibles con Outlook como gifs y carruseles. La compatibilidad general es buena.

---

## DOCUMENTACIÓN FINAL

### Guía de usuario

1. Abre tu newsletter (revisa spam si no aparece).
2. Lee la información del evento.
3. Haz clic en el botón “Más información” en cada sección.

### Informe final del proyecto

Este proyecto busca aumentar el alcance del Salón del Cómic de València, combinando newsletters con campañas en redes sociales.

El diseño se enfoca en un formato minimalista y modular.

El mayor reto técnico fue el envío automatizado con Node.js, aprendido desde cero.

El feedback de los usuarios ha sido esencial para mejorar la calidad del trabajo.

---
