UTEZ | Grupo 2°D — Tarea Integradora — Equipo 13
Integrantes
Usuario GitHubRamaSant04535santiago-martinez axel-dsaxel-ernesto

Descripción del sistema
Aplicación de escritorio desarrollada en Java + JavaFX que permite a un consultorio pequeño administrar su directorio de pacientes. Implementa un CRUD completo con persistencia en archivo .csv, sin uso de base de datos.

Funcionalidades principales

Alta: Registrar nuevos pacientes mediante formulario con validaciones.
Consulta: Visualizar todos los pacientes en una tabla interactiva.
Actualización: Editar los datos de un paciente seleccionado.
Eliminación lógica: Cambiar estatus a INACTIVO en lugar de borrar físicamente.
Persistencia: Los datos se guardan en pacientes.csv y se conservan al reiniciar la app.
Resumen en pantalla: Contador de Total / Activos / Inactivos actualizado en tiempo real.


Estructura del proyecto
utez-2d-pacientes-javafx-equipo14/
└── Consultorio/
    ├── src/
    │   └── main/
    │       ├── java/
    │       │   └── org.example.consultorio/
    │       │       ├── HelloApplication.java
    │       │       ├── HelloController.java
    │       │       ├── Launcher.java
    │       │       ├── module-info.java
    │       │       ├── model/
    │       │       │   └── Paciente.java
    │       │       ├── repository/
    │       │       │   └── PacienteRepository.java
    │       │       └── service/
    │       │           └── PacienteService.java
    │       └── resources/
    │           └── org.example.consultorio/
    │               └── hello-view.fxml
    ├── .gitignore
    ├── mvnw
    ├── mvnw.cmd
    ├── pom.xml
    └── README.md

Tecnologías utilizadas
TecnologíaVersiónJava17+JavaFX17+IDEIntelliJ IDEAPersistenciaArchivo .csv

Cómo ejecutar el proyecto
Requisitos previos

Java JDK 17 o superior instalado.
IntelliJ IDEA (Community o Ultimate).

Pasos

Clonar el repositorio:

bashgit clone https://github.com/Sant04535/utez-2d-pacientes-javafx-equipo14.git
cd utez-2d-pacientes-javafx-equipo14

Abrir en IntelliJ IDEA:

File > Open → seleccionar la carpeta Consultorio (donde está el pom.xml).
IntelliJ detectará el proyecto Maven automáticamente.


Colocar el archivo de datos:

Asegúrate de que pacientes.csv esté en la raíz del proyecto junto al pom.xml.
Si no existe, el programa lo crea automáticamente en la primera ejecución.


Ejecutar:

Correr la clase Launcher.java.


Git Flow
main
  └── dev
        ├── santiago-martinez
        └── axel-ernesto

Cada integrante trabaja y commitea en su rama personal.
Al tener una funcionalidad lista, se hace merge a dev.
Se prueba en dev que todo funcione correctamente.
Al finalizar el proyecto, merge de dev a main.
