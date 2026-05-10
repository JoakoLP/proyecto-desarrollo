# Product Backlog: Sistema para Posgrado

**Integrantes:** 
* Franco Esperanza
* Matias Goya
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

| ID | Épica | Historia de Usuario | Criterios de Aceptación | SP | Prior. | Sprint |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **US-01** | EP-01 | Como *aspirante*, quiero acceder a un formulario web, para inscribirme sin enviar correos. | Dado que ingresa al enlace, cuando completa los campos, entonces los datos se guardan. | 5 | M | 1 |
| **US-02** | EP-01 | Como *aspirante*, quiero adjuntar mis documentos en PDF, para completar mi legajo digital. | Dado que selecciona archivos, cuando los sube, entonces el sistema los valida y almacena. | 3 | M | 1 |
| **US-03** | EP-01 | Como *conducción*, quiero ver el estado del legajo con indicador visual, para saber si está completo. | Dado que accede al panel, cuando revisa el aspirante, entonces ve un indicador de completitud. | 3 | M | 2 |
| **US-04** | EP-02 | Como *conducción*, quiero registrar asistencia y notas del estudiante, para actualizar su estado académico. | Dado que ingresa las notas, cuando las confirma, entonces se actualiza el perfil del estudiante. | 5 | M | 2 |
| **US-05** | EP-03 | Como *docente*, quiero acceder a mi planilla vía enlace, para cargar asistencia sin usuario/contraseña. | Dado que recibe el link, cuando lo abre, entonces ve su planilla activa del seminario. | 3 | S | 3 |
| **US-06** | EP-02 | Como *CPR*, quiero registrar los datos del Trabajo Final o Tesis (título, director, resolución), para mantener el seguimiento del estudiante. | Dado que el estudiante tiene un tema aprobado, cuando la CPR ingresa los datos, entonces se reflejan en su legajo. | 5 | M | 2 |
| **US-07** | EP-03 | Como *conducción*, quiero que el sistema envíe recordatorios automáticos a los docentes, para asegurar la carga de notas en tiempo y forma. | Dado que se acerca la fecha límite de carga, cuando el sistema detecta que faltan notas, entonces envía un email al docente. | 5 | S | 3 |
| **US-08** | EP-03 | Como *docente*, quiero descargar mi planilla en formato analógico, para tener un respaldo físico durante las clases. | Dado que visualizo mi planilla, cuando hago clic en descargar, entonces se genera un archivo imprimible. | 2 | C | 4 |
| **US-09** | EP-04 | Como *conducción*, quiero acceder a un módulo de estadísticas por cohorte, para analizar inscripciones, graduados y desgranamiento. | Dado que ingreso al módulo de reportes, cuando selecciono una cohorte, entonces visualizo los gráficos y métricas de estado. | 8 | S | 4 |
