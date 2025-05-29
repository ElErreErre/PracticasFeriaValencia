# RETO FERIA VALENCIA  
## SUPUESTO 3  

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

Analizando el mercado, hemos dividido al público en distintos grupos:

- **Expositores con Experiencia Previa en Expojove (Expositores Recurrentes)**  
- **Nuevos Expositores o Expositores con Poca Experiencia**  
- **Expositores que Buscan Servicios Específicos o Avanzados**  

Debemos focalizar la newsletter a expositores **nuevos**, ya que no son conocedores de nuestros servicios, lo que puede abrir la puerta a contrataciones.

### DAFO y competencia

**Fortalezas:**

- Conocimiento del Público Expositor  
- Variedad y Calidad de Servicios  

**Debilidades:**

- Complejidad de los Servicios  
- Capacidad de Soporte Limitada  

**Oportunidades:**

- Tecnología para la Automatización  
- Tendencias Digitales  
- Nuevos Expositores Potenciales  

**Amenazas:**

- Problemas Técnicos/Plataforma  
- Competencia de Otros Eventos/Ferias  

### Objetivo de la campaña

**Comunicación de Servicios a Expositores de ExpoJove**  
El objetivo primordial es asegurar que todos los expositores comprendan y utilicen eficientemente la gama completa de servicios disponibles, optimizar el proceso de solicitud, reducir la carga de soporte, y reforzar la percepción de Expojove como un evento bien organizado.

---

## DISEÑO

### Mockup

Mockup realizado con **Figma**. Se ha centrado en la cabecera y el footer; el resto está representado con bloques de imágenes y texto *Lorem Ipsum*.

### Responsive avanzado con MJML

MJML incluye responsive por defecto. Se esperó al feedback del *user testing* para detectar problemas, pero no hubo quejas.

---

## TEST CON USUARIOS

Se ha realizado con alumnos, profesores y amigos mediante un **Google Forms** con escala del 1 al 5.  
Aún no se ha hecho rediseño, pero se sigue abierto a recibir feedback constructivo.

---

## DESARROLLO Y ENVÍO DE CORREOS

Usando **AWS EC2 + Node.js + MJML**:

1. Lanzamiento de instancia EC2 (Ubuntu) y conexión por SSH.  
2. Instalación de **MySQL**, creación de base de datos y usuario.  
3. Instalación de **Node.js**, **npm** y librerías:  
   - `nodemailer` (envío de correos)  
   - `mysql2` (interacción con BBDD)  
   - `mjml` (plantillas de correo)  
4. Archivo `.env` para credenciales seguras.  
5. Envío ejecutando `node app.js`.  
6. Pruebas realizadas con cuentas de Gmail y Outlook (inicialmente llegan a SPAM).  

Repositorio con detalles:  
🔗 [GitHub - PracticasFeriaValencia](https://github.com/ElErreErre/PracticasFeriaValencia)

---

## INTEGRACIÓN CON REDES SOCIALES

Descartada la idea de crear vídeos por su escaso impacto en un nicho tan específico.  
Se opta por **campañas publicitarias en TikTok e Instagram Reels**, que permiten alcanzar al público objetivo sin depender de algoritmos.

---

## CONTROL DE VERSIONES CON GITHUB

Se utiliza Git desde **Visual Studio Code**.  
Commits regulares según el avance y el feedback recibido.

---

## PERSONALIZACIÓN DEL CORREO MJML

El archivo `app.js` permite definir un **asunto personalizado** y contenido dinámico como `{nombre}` que se reemplaza con datos reales de la base de datos.

---

## VERIFICAR COMPATIBILIDAD CON DIFERENTES CLIENTES DE CORREO

Pruebas realizadas con Gmail y Outlook.  
Se evitó el uso de elementos no compatibles con Outlook (como GIFs o carruseles).

---

## DOCUMENTACIÓN FINAL

### Guía de usuario

1. Abre tu Newsletter.  
2. Lee la información sobre los servicios.  
3. Haz clic en el botón **"Accede al Portal del Expositor"**.  
4. Contrata los servicios según interés.  

### Informe final del proyecto

El objetivo es atraer nuevos expositores.  
Se combina la **newsletter** con **campañas en redes sociales**.  
Se ha optado por un diseño **minimalista y modular**.  
El envío automatizado ha sido el mayor reto técnico.  
El *user testing* ha sido clave para mejorar la calidad final.

---
