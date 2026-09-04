# DOSW__ParcialT1_JavierCaicedo
Examen 1 - 04/09/26

# 1. Diagrama de contexto:
Construya el Diagrama de Contexto C4 del sistema. 

![Diagrama de contexto C4](../docs/images/context.png)

# 2. Requerimientos 
Identifique 5 requerimientos del sistema y clasifíquelos en funcionales (3) y no funcionales (2). Garantice que al menos un requerimiento funcional utilice un patrón de diseño que 
definirá más adelante.

# Requerimientos FUNCIONALES del Sistema
  ### 2.1 Requerimiento Funcional 1

| Campo | Descripción |
|------|-------------|
| **ID** | RF-01 |
| **Nombre del requerimiento** | Consulta de horarios de tutorias |
| **Descripción** | El sistema permite a un usuario consultar los horarios de tutorias con los diferentes Tutores disponibles, siempre y cuando el usuario se encuentra habilitado para acceder a la información de la materia. |
| **Precondiciones** | Para que el sistema cumpla con este requerimiento, TutoECI debe tener previamente un autenticado al usuario con credenciales válidas (nombre de usuario y contraseña). |
| **Actor** | Estudiante, Tutor |
| **Flujo principal** | 1. El Estudiante/Tutor inicia sesión en el sistema con sus credenciales.<br>2. El etudiante/tutor selecciona la opción de consultar tutorias.<br>3. El sistema valida si el usuario tiene acceso a la materia consultada(en este caso se da acceso)<br>4. El estudiante/tutor elige la franja horaria o tutor deseado.<br>5. El sistema solicita los datos necesarios según la acción (fechas, tutor, prioridad, etc).<br>6. El sistema ejecuta la acción y muestra la informacion general de las tutorias según filtración. |
| **Diagrama de caso de uso** | ![Diagrama de caso de uso - Consulta horarios](../uml/RF1-CU.png) |
| **Poscondiciones** | Se espera como resultado que se la muestre al usuario la informacion solicitada según sus intereses. |
| **Historia de usuario** | COMO estudiante QUIERO solicitar las franjas horarias de las tutorias de las materias que estoy viendo PARA PODER realizar la solicitud de la tutoria de acuerdo a mis intereses y necesidades |

  ### 2.2 Requerimiento Funcional 2

| Campo | Descripción |
|------|-------------|
| **ID** | RF-02 |
| **Nombre del requerimiento** | Notificar al usuario, cumpliendo con el formato indicado |
| **Descripción** | El sistema notifica al usuario en caso de que su reserva haya sido realizada de manera correcta. |
| **Precondiciones** | 1. Para que el sistema cumpla con este requerimiento, TutoECI debe tener previamente un autenticado al usuario con credenciales válidas (nombre de usuario y contraseña). 2. El usuario debió haber creado una solicitud de reserva hacia esa materia. |
| **Actor** | Estudiante |
| **Flujo principal** | 1. El Estudiante inicia sesión en el sistema con sus credenciales.<br>2. El etudiante selecciona la opción de solicitar tutorias.<br>3. El sistema valida si el usuario tiene acceso a la materia consultada(en este caso se da acceso)<br>4. El estudiante elige la franja horaria o tutor deseado.<br>5. El sistema solicita los datos necesarios según la acción (fechas, tutor, prioridad, etc).<br>6. El sistema ejecuta la acción y realiza la reserva.<br>5. Se envía la notificacion en el formato: correo@mail.escuelaing.edu.co|Mensaje_de_confirmacion. |
| **Diagrama de caso de uso** | ![Diagrama de caso de uso - Notificacion de confirmacion](../uml/RF2-CU.png) |
| **Poscondiciones** | Se espera como resultado que quede en la bandeja de notificaciones el respectivo mensaje |
| **Historia de usuario** | COMO estudiante QUIERO tener la notificacion de confirmacion de la reserva realizada PARA PODER tener la certeza de asistir a la tutoria de manera adecuada. |


  ### 2.3 Requerimiento Funcional 3

| Campo | Descripción |
|------|-------------|
| **ID** | RF-02 |
| **Nombre del requerimiento** | Permitir solicitar tutorias de maneras diferentes |
| **Descripción** | El sistema permite al usuario solicitar tutorias de maneras diferentes dependiendo de sus requerimientos y prioridades(FASTEST_AVAILABLE / EXPERT_FIRST / PEER_TUTORING) |
| **Precondiciones** | 1. Para que el sistema cumpla con este requerimiento, TutoECI debe tener previamente un autenticado al usuario con credenciales válidas (nombre de usuario y contraseña). |
| **Actor** | Estudiante |
| **Flujo principal** | 1. El Estudiante inicia sesión en el sistema con sus credenciales.<br>2. El etudiante selecciona la opción de solicitar tutorias.<br>3. El sistema valida si el usuario tiene acceso a la materia consultada(en este caso se da acceso)<br>4. El estudiante elige la opcion de filtrado de solicitud deseada(FASTEST_AVAILABLE / EXPERT_FIRST / PEER_TUTORING).<br>5. El sistema solicita los datos necesarios según la acción (fechas, tutor, prioridad, etc).<br>6. El sistema ejecuta la acción y realiza la reserva de acuerdo a la opcion escogida. |
| **Diagrama de caso de uso** | ![Diagrama de caso de uso - SOlicitud con requerimientos](../uml/RF3-CU.png) |
| **Poscondiciones** | Se espera como resultado que quede debidamente reservado en la base de datos la franja horaria correspondiente a la materia y al tutor. |
| **Historia de usuario** | COMO estudiante QUIERO solicitar de diferentes maneras la opción de tutoria dependiendo de mis prioridades y requerimientos PARA PODER tener una mejor tutoria frente a mis necesidades en la materia solicitada. |


# Requerimientos no funcionales:
  - La pagina debe respetar la identidad institucional incluyento la paleta de colores oficial del programa
  - Se debe emplear una tipografia clara con unos estandares minimos al contraste


# 3. Jira - Planeación Agile 
Seleccione el requerimiento principal (Recomendación de Tutor) y realice la 
descomposición. En Jira registre: 
• 1 Épica. 
• La Historia de Usuario obligatoria. 
• Mínimo 3 tareas técnicas (ej. refactorización, lógica de selección, conexión a 
sistemas externos). 

Link de JIRA: https://mail-team-auscl79v.atlassian.net/jira/software/projects/PAR/boards/2/timeline?selectedIssue=PAR-2&atlOrigin=eyJpIjoiMGY2ZDM5MWM0NTUxNDQxOWI0MWZiZDI1YWY1YjdiODgiLCJwIjoiaiJ9

imagenes referentes a la creacion y a las relacion de subtareas:

![Imagen1 - Creaciones en JIRA](../images/JR1.png)
![Imagen2 - Realciones en JIRA](../images/JR2.png)

# 4. Patrones de diseño 

Identifique 2 patrones de diseño aplicables a este caso de estudio (por ejemplo, uno para 
la estrategia de selección de preferencia y otro para aislar la interoperabilidad con los 
sistemas externos). Especifique: 
• Nombre del patrón. 
• Tipo de patrón (creacional, estructural o de comportamiento). 
• Justificación de la decisión.  
Realice un Diagrama de Clases que permita entender su solución y mencione 
explícitamente qué principios SOLID está aplicando y por qué. (Añada el diagrama y la 
justificación al README).

### 4.1 Patrón COMMAND

| Nombre | Command |
|------|-------------|
| **TIPO** | Comportamiento |
| **JUSTIFCACION** | Se analiza la implementacion de este patrón precisamente en el requisito funcional obligatorio, buscando como fin que dependiendo del ingreso que se le da a la solicitud que puede ser de 3 tipos:FASTEST_AVAILABLE / EXPERT_FIRST / PEER_TUTORING , se analiza que dependiendo del requerimiento que solicite el estudiante, se realiza un proceso diferente a pesar de que la acción sigue siendo solicitar una tutoria, de este modo se agiliza y se generaliza una solicitud para luego ser implementado en forma de interfaz por las solicitudes especificas, de este modo manejan las mismas operaciones generales, pudiendo tener cada una un filtro y una respuesta diferente de acuerdo a su linea de busqueda. |

| Nombre | Adapter |
|------|-------------|
| **TIPO** | Creacional |
| **JUSTIFCACION** | Se analiza la implementacion de este patrón devido a que se debe hacer uso de el formato JSON para transportar informacion desde enlace, esto significa que estamos recibiendo un tipo de archivo que debe ser adaptado para su debida validacion y su debido filtrado dentro de la implementacion final para tener un flujo de informacion manejable dentro del servicio y no ser dependientes de otro 3er servicio o aplicacion para poder realizar la conversion de información. |

Diagrama de clases:
![Imagen2 - Diagrama de clases](../uml/DC-Base.png)