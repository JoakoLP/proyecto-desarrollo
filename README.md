# Product Backlog: Sistema para Posgrado

**Integrantes:** 
* Franco Esperanza
* Matias Goya Campanella
* Franco Pagani
* Joaquín Takara
* Rubén Veliz


**Fecha:** 10 de mayo de 2026

**Materia:** Desarrollo de Software S34 - UTN

---

## Contexto, Actores y Épicas

El sistema reemplazará la gestión manual (correos y Excel) por una plataforma web centralizada para posgrados.

### Actores Identificados:
* **Aspirante:** Se inscribe a la carrera.
* **Estudiante:** Cursa la carrera.
* **Docente:** Carga asistencia y notas.
* **Conducción / CPR:** Administra y supervisa.

### Épicas del Sistema:
* **EP-01:** Gestión de Inscripciones.
* **EP-02:** Legajo y Perfil Académico.
* **EP-03:** Gestión Docente.
* **EP-04:** Estadísticas y Reportes.
* **EP-05:** Administración del Sistema.

---

## Estructura del Product Backlog

| ID | Épica | Historia de Usuario | Criterios de Aceptación | SP | Prioridad | Sprint |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **US-01** | EP-01 | **Como** aspirante, **quiero** completar un formulario de preinscripción online, **para poder** iniciar el proceso de admisión sin enviar correos. | **C1:** Dado que el aspirante ingresa al formulario, Cuando completa todos los campos obligatorios, Entonces los datos se guardan exitosamente.<br><br>**C2:** Dado que el aspirante omite campos requeridos, Cuando intenta enviar el formulario, Entonces el sistema resalta los errores y no lo envía. | 5 | Must | 1 |
| **US-02** | EP-01 | **Como** aspirante, **quiero** adjuntar mis documentos requeridos en PDF, **para poder** completar mi legajo digital. | **C1:** Dado que el aspirante selecciona archivos en formato PDF, Cuando presiona subir, Entonces el sistema almacena los documentos en su legajo.<br><br>**C2:** Dado que el aspirante intenta subir una imagen JPG, Cuando intenta cargarla, Entonces el sistema rechaza el formato indicando que solo admite PDF. | 3 | Must | 1 |
| **US-03** | EP-01 | **Como** conducción, **quiero** revisar la documentación de los aspirantes, **para poder** validar que cumplan con los requisitos de inscripción. | **C1:** Dado que la conducción accede al listado de aspirantes, Cuando selecciona un perfil, Entonces puede visualizar y descargar los documentos adjuntos.<br><br>**C2:** Dado que la conducción revisa un legajo completo, Cuando lo aprueba, Entonces el estado del aspirante cambia a verificado. | 5 | Must | 1 |
| **US-04** | EP-01 | **Como** conducción, **quiero** abrir y cerrar los períodos de inscripción, **para poder** controlar el ingreso de nuevos aspirantes por cohorte. | **C1:** Dado que la conducción configura las fechas de inscripción, Cuando llega la fecha de inicio, Entonces el formulario se habilita públicamente.<br><br>**C2:** Dado que el período está cerrado, Cuando un usuario intenta acceder al enlace, Entonces el sistema muestra una pantalla de inscripción finalizada. | 3 | Should | 1 |
| **US-05** | EP-02 | **Como** conducción, **quiero** buscar estudiantes inscriptos de forma individual o por cohorte, **para poder** gestionar su información rápidamente. | **C1:** Dado que la conducción ingresa a la búsqueda, Cuando filtra por cohorte, Entonces el sistema lista todos los estudiantes de ese ciclo lectivo.<br><br>**C2:** Dado que la conducción busca por nombre, Cuando no hay coincidencias, Entonces el sistema muestra el mensaje "No se encontraron estudiantes". | 3 | Must | 2 |
| **US-06** | EP-02 | **Como** conducción, **quiero** visualizar el perfil académico del estudiante, **para poder** consultar su cohorte, estado del legajo y seminarios. | **C1:** Dado que la conducción accede al perfil de un estudiante, Cuando los datos cargan, Entonces visualiza la cohorte a la que pertenece y su estado actual.<br><br>**C2:** Dado que el perfil se muestra en pantalla, Cuando revisa la sección académica, Entonces observa la lista de materias y seminarios en curso. | 5 | Must | 2 |
| **US-07** | EP-02 | **Como** conducción, **quiero** consultar el porcentaje de asistencia de un estudiante en un seminario, **para poder** determinar si cumple con el mínimo requerido. | **C1:** Dado que el docente cargó las asistencias, Cuando la conducción revisa el seminario, Entonces el sistema calcula y muestra el porcentaje de asistencia.<br><br>**C2:** Dado que el estudiante tiene menos del porcentaje mínimo, Cuando se visualiza el reporte, Entonces el sistema lo resalta como no regular. | 5 | Must | 2 |
| **US-08** | EP-02 | **Como** conducción, **quiero** registrar la fecha del acta de examen junto a la calificación, **para poder** oficializar la nota en el sistema institucional. | **C1:** Dado que la conducción ingresa una nota final, Cuando agrega una fecha de acta válida, Entonces la calificación se oficializa en el perfil del estudiante.<br><br>**C2:** Dado que se intenta guardar una nota, Cuando se omite la fecha del acta, Entonces el botón de guardar se deshabilita. | 3 | Must | 2 |
| **US-09** | EP-02 | **Como** conducción, **quiero** registrar las instancias de tutorías, **para poder** monitorear el avance del estudiante. | **C1:** Dado que ocurre una tutoría, Cuando la conducción ingresa los detalles y la fecha, Entonces la sesión queda registrada en el historial del estudiante.<br><br>**C2:** Dado que se registra un seguimiento, Cuando el texto supera los caracteres permitidos, Entonces el sistema recorta el mensaje y lanza una advertencia. | 2 | Could | 3 |
| **US-10** | EP-02 | **Como** CPR, **quiero** cargar los datos de la Tesis o TFI (título, director, nro resolución), **para poder** formalizar la finalización de la carrera. | **C1:** Dado que el estudiante entra en etapa de tesis, Cuando la CPR ingresa título y director, Entonces los datos se asocian permanentemente a su legajo.<br><br>**C2:** Dado que la CPR guarda la información, Cuando el campo "Número de resolución" está vacío, Entonces el sistema exige completarlo para avanzar. | 5 | Must | 2 |
| **US-11** | EP-03 | **Como** docente, **quiero** acceder a la planilla de mi seminario, **para poder** visualizar el listado de inscriptos con sus correos y carrera. | **C1:** Dado que el docente hace clic en su enlace de acceso, Cuando el enlace es válido, Entonces ve la lista completa de sus alumnos inscriptos.<br><br>**C2:** Dado que un seminario no tiene inscriptos aún, Cuando el docente abre la planilla, Entonces el sistema muestra una lista con encabezados vacía. | 3 | Must | 3 |
| **US-12** | EP-03 | **Como** docente, **quiero** cargar la asistencia y notas de mis alumnos en la plataforma, **para poder** informar su desempeño académico a la conducción. | **C1:** Dado que el docente está en la planilla, Cuando ingresa una calificación numérica válida, Entonces el sistema actualiza el registro exitosamente.<br><br>**C2:** Dado que el docente ingresa un valor fuera de rango (ej. mayor a 10), Cuando intenta guardar, Entonces la celda marca un error de validación. | 5 | Must | 3 |
| **US-13** | EP-03 | **Como** docente, **quiero** descargar mi planilla con los estudiantes inscriptos en formato analógico, **para poder** utilizarla de manera impresa en clases. | **C1:** Dado que el docente visualiza su planilla activa, Cuando hace clic en el botón descargar, Entonces el sistema genera un archivo PDF.<br><br>**C2:** Dado que se descarga el archivo, Cuando el docente lo abre, Entonces visualiza columnas para apellido, nombre, correo y carrera. | 2 | Could | 4 |
| **US-14** | EP-03 | **Como** conducción, **quiero** que el sistema envíe recordatorios automáticos a los docentes, **para poder** garantizar la carga de notas en tiempo y forma. | **C1:** Dado que se acerca la fecha límite de carga, Cuando faltan notas por registrar en un seminario, Entonces el sistema dispara un email de alerta al docente.<br><br>**C2:** Dado que la planilla ya está 100% completa, Cuando llega la fecha límite, Entonces el sistema omite el envío de recordatorios para ese docente. | 5 | Should | 4 |
| **US-15** | EP-04 | **Como** conducción, **quiero** acceder a un módulo de estadísticas, **para poder** analizar el desgranamiento, inscripciones y ralentización por cohorte. | **C1:** Dado que la conducción accede al módulo, Cuando selecciona una cohorte específica, Entonces visualiza el total de inscripciones y graduados mediante gráficos.<br><br>**C2:** Dado que existen alumnos inactivos, Cuando se consulta el nivel de desgranamiento, Entonces el sistema calcula y exhibe el porcentaje de abandono general. | 8 | Should | 4 |
| **US-16** | EP-02 | **Como** estudiante, **quiero** visualizar mis calificaciones y el porcentaje de asistencia por seminario, **para poder** llevar un seguimiento personal de mi desempeño académico. | **C1:** Dado que el estudiante accede a su perfil, Cuando ingresa a la sección de seminarios, Entonces visualiza la lista de materias cursadas con sus notas finales y porcentaje de asistencia.<br><br>**C2:** Dado que un seminario aún no finalizó, Cuando el estudiante revisa esa materia, Entonces el sistema muestra el estado como "En curso" en lugar de una calificación. | 3 | Should | 3 |
| **US-17** | EP-02 | **Como** estudiante, **quiero** consultar los datos oficiales de mi Trabajo Final o Tesis (título, director, resolución), **para poder** verificar que mi trámite fue aprobado y registrado por la CPR. | **C1:** Dado que la CPR cargó los datos de la tesis, Cuando el estudiante accede a su perfil de graduación, Entonces visualiza el título, los directores y el número de resolución oficial.<br><br>**C2:** Dado que el estudiante aún no tiene un tema aprobado, Cuando ingresa a la sección de Tesis, Entonces el sistema muestra el mensaje informativo "Aún no posee datos de tesis registrados". | 2 | Could | 4 |
| **US-18** | EP-02 | **Como** estudiante, **quiero** acceder a los datos administrativos de mi cursada (cohorte actual y estado del legajo), **para poder** confirmar que mi situación y documentación se encuentran en regla. | **C1:** Dado que el estudiante inicia sesión, Cuando va a la sección de datos personales, Entonces visualiza a qué cohorte pertenece y su estado general (ej. Regular).<br><br>**C2:** Dado que el legajo del estudiante tiene documentación pendiente, Cuando revisa su estado, Entonces el sistema le muestra una alerta indicando que debe comunicarse con administración para completar su expediente. | 3 | Should | 3 |
| **US-19** | EP-02 | **Como** conducción, **quiero** ver un indicador tipo semáforo y alertas de vencimiento en el perfil del estudiante, **para poder** monitorear visualmente su estado de avance y plazos límite. | **C1:** Dado que la conducción accede al perfil de un estudiante, Cuando el alumno está próximo a vencer el plazo de un seminario, Entonces el sistema muestra una alerta visual en color rojo.<br><br>**C2:** Dado que un estudiante ingresa a su propio perfil, Cuando intenta buscar su indicador de avance o semáforo, Entonces el sistema oculta esta información ya que es de acceso restringido para la conducción. | 5 | Must | 2 |
| **US-20** | EP-01 | **Como** aspirante, **quiero** registrarme e iniciar sesión vinculando mi cuenta de Google, **para poder** evitar crear y recordar una nueva contraseña. | **C1:** Dado que el aspirante está en la pantalla de inicio, Cuando hace clic en "Ingresar con Google", Entonces el sistema le solicita los permisos básicos de su cuenta.<br><br>**C2:** Dado que el aspirante completó la vinculación con Google, Cuando el sistema recibe la autorización, Entonces extrae su correo electrónico y crea su perfil automáticamente. | 3 | Won't | - |
