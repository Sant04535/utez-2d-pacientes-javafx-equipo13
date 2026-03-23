UTEZ | Grupo 2°D
Tarea Integradora — Equipo 14


Integrantes
Sant04535 (santiago-martinez) axel-ds (axel-ernesto)

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
Consultorio
├── src/
│   └── main/
│       ├── java/
│       │   └── org.example.consultorio/
│       │       ├── HelloApplication.java
│       │       ├── HelloController.java
│       │       ├── Launcher.java
│       │       └── module-info.java
│       └── resources/
│           └── org.example.consultorio/
│               ├── app-view.fxml
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
JavaFX SDK 17 descargado (gluonhq.com/products/javafx).
IntelliJ IDEA (Community o Ultimate).

Pasos

Clonar el repositorio:

bash   git clone https://github.com/Sant04535/utez-2d-pacientes-javafx-equipo14.git
   cd utez-2d-pacientes-javafx-equipo14
```

2. **Abrir en IntelliJ IDEA:**
   - `File > Open` → seleccionar la carpeta del proyecto.

3. **Configurar JavaFX en IntelliJ:**
   - `File > Project Structure > Libraries` → añadir la carpeta `lib` del JavaFX SDK.
   - En `Run > Edit Configurations`, agregar en VM options:
```
     --module-path /ruta/a/javafx-sdk/lib --add-modules javafx.controls,javafx.fxml
```

4. **Ejecutar:**
   - Correr la clase `Main.java`.

---

## Archivo de datos de prueba

El archivo `resources/pacientes.csv` incluye 5 pacientes de prueba con el formato:
```
CURP,Nombre,Edad,Teléfono,Alergias,Estatus
MARG900101HDFRRN09,Carlos García Ramos,34,5512345678,Penicilina,ACTIVO
LOPJ850215MDFPZR04,Juana López Pérez,40,5598765432,Ninguna,ACTIVO
VAMX001120HDFLLR05,Maximiliano Vázquez,24,5567891234,Polen,INACTIVO
RONA750303MDFDRN07,Ana Rodríguez Nieto,50,5543217890,Ibuprofeno,ACTIVO
HERG991231HDFRRR02,Roberto Herrera García,26,5511223344,Ninguna,ACTIVO
```

---

## Git Flow
```
main
 └── dev
      ├── santiago-martinez
      └── axel-ernesto

Cada integrante trabaja y commitea en su rama personal.
Al tener una funcionalidad lista, se hace merge a dev.
Se prueba en dev que todo funcione.
Al finalizar el proyecto, merge de dev a main.


Criterios cubiertos

 CRUD completo
 Persistencia en archivo .csv
 Validaciones (campos vacíos, nombre, edad, teléfono, CURP duplicado)
 Estatus ACTIVO / INACTIVO (borrado lógico)
 Resumen Total / Activos / Inactivos
 POO: modelo Paciente, servicio PacienteService
 ObservableList para el TableView
 try/catch para IO y validaciones
