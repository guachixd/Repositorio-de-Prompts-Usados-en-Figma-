# Repositorio-de-Prompts-Usados-en-Figma-
# 1. Como Product Owner quiero definir los requerimientos de acceso al sistema para que los usuarios puedan ingresar de forma segura según su rol.
# Fine-Tuned English (FTE+) — Prototipo UX/UI

Prototipo de alta fidelidad (mobile-first) de **Fine-Tuned English**, una plataforma de capacitación corporativa en línea donde los colaboradores acceden a sus cursos asignados, rinden evaluaciones y obtienen certificados, mientras RRHH y Administración gestionan usuarios, cursos y reportes.

## Historia de Usuario

> **Como** Product Owner
> **quiero** definir los requerimientos de acceso al sistema
> **para que** los usuarios puedan ingresar de forma segura según su rol.

Este requerimiento se tradujo en el flujo de **Login → Regístrate aquí → Completar formulario → Registrarse → Registro Exitoso → Volver al Inicio**, donde cada usuario solo visualiza las funcionalidades correspondientes a su perfil dentro del sistema.

## Objetivo del prototipo

Validar la navegabilidad, comprensión, eficiencia y satisfacción de los usuarios frente al flujo de acceso y a las funcionalidades principales de la plataforma, antes de pasar a desarrollo.

## Roles contemplados en el diseño

| Rol | Acceso en el prototipo |
|---|---|
| **Estudiante / Colaborador** | Mis Cursos Asignados, Mis Certificados, Mi Perfil |
| **Admin RRHH** | Todo lo anterior + Reportes y KPIs |
| **Super Admin** | Todo lo anterior + Gestión de Usuarios y Gestión de Cursos |

## Flujo de Acceso

1. **Login** — correo institucional + contraseña.
2. **Registro** — nombre, correo, cédula, fecha de nacimiento y departamento (Docente / Administrativo).
3. **Registro Exitoso** — la cuenta queda en estado *"Esperando Aprobación"* hasta validación de un Administrador.
4. **Acceso al Portal** — según el rol asignado, el usuario es dirigido a su dashboard correspondiente.

## Pantallas diseñadas

- Login / Registro / Registro Exitoso
- Dashboard del estudiante (cursos asignados)
- Detalle de curso
- Reproductor de curso (video, prácticas, tabs de descripción/reseñas/bibliografía)
- Evaluación (quiz) con temporizador y resultado
- Mis certificados
- Mi perfil
- Gestión de usuarios — *Super Admin*
- Gestión de cursos — *Super Admin*
- Reportes y KPIs — *Admin RRHH*

## Pruebas de usabilidad

Se realizaron pruebas con usuarios reales sobre el flujo de Registro e Inicio de Sesión, evaluando cuatro dimensiones: **Navegabilidad, Comprensión, Eficiencia y Satisfacción**, registrando hallazgos en una matriz de retroalimentación por participante.

## Herramientas utilizadas

- **Figma** — diseño UI y prototipo interactivo
- **Maze** — pruebas de usabilidad
- **Miro** — Matriz de Impacto-Esfuerzo y planificación

## Estado del proyecto

Prototipo de diseño en fase de validación con usuarios, pendiente de ajustes según hallazgos antes de pasar a la etapa de desarrollo.

# 2. Como UX Researcher quiero diseñar el flujo de acceso al sistema para garantizar una experiencia de login intuitiva y sin fricciones.
link del diagrama: https://drive.google.com/file/d/11VTgmf6Zy6t34HMXiAfbeAjsJbO7S1dX/view?usp=sharing
# 3. Como Scrum Master quiero planificar el Sprint 7 y registrar las ceremonias para mantener el seguimiento del avance en autenticación y 4. Como equipo queremos usar IA para optimizar el diseño del módulo de gestión de usuarios y generar casos de uso adicionales.
Realizamos reuniones de 25 minutos diarios donde pudimos hacer el siguiente, donde usamos los siguiente prompts: 
-Mira tengo que hacer esto, pero como ves necesito el fijma para hacerlo por eso en base a esos bocetos y a esos colores que puedes ver queria crear el fijma para hacer eso es una plataforma de e learning si hay algo q no entiendas preguntamelo y te lo aclaro. Te recuerdo no quiero la actividad solo el Fijma y estos son los colores de mi cliente Fine online
#0d63a7
#e40054
#004784
#f4f4f4
Colores institucionales
#213354
#e40054
-Actúa como un Diseñador UI/UX Senior y Desarrollador Frontend Experto. Quiero que crees un prototipo web interactivo móvil-first de alta fidelidad para una plataforma de e-learning llamada "Fine-Tuned English" (o "Fine Online"), basándote en los bocetos a mano que te adjunto y las siguientes especificaciones técnicas y visuales.

El entregable debe estructurarse como una aplicación de una sola página (Single Page Application - SPA) estática usando HTML5 semántico, CSS3 Vanilla (con estilos premium y modernos) y JavaScript nativo (para controlar la reactividad, simulación y estados del prototipo).

---

### 🎨 1. IDENTIDAD VISUAL Y DISEÑO (BRANDING)
Aplica la siguiente paleta de colores corporativos del cliente para dar una estética de alta fidelidad, premium y profesional:
- Color Primario (Azul): #0d63a7 (usado para la marca, botones primarios y acentos corporativos).
- Color de Acento (Fucsia): #e40054 (usado para acciones críticas, botones destacados y estados activos).
- Color Azul Oscuro / Corporativo: #004784 y #213354.
- Fondo de la aplicación: #f4f4f4 (gris muy claro limpio).
- Tarjetas y Contenedores: #ffffff con esquinas redondeadas (border-radius: 12px a 18px) y sombras suaves (box-shadow elegante).
- Tipografía: Importa y usa la fuente 'Inter' de Google Fonts.
- Estética General: Diseños limpios, efectos sutiles de glassmorphism (transparencias con backdrop-filter) en encabezados y barra lateral, y micro-animaciones fluidas en hovers de botones y transiciones de pantalla.

---

### 📱 2. FORMATO DEL DISPOSITIVO
- El diseño debe ser Mobile-First (optimizado y centrado para la pantalla de un smartphone).
- Integra un contenedor o "canvas móvil" centrado en el navegador de escritorio para que parezca una pantalla de celular real durante la simulación y pruebas de usabilidad (por ejemplo en Maze).

---

### 🧩 3. PANTALLAS Y FLUJOS A IMPLEMENTAR
El prototipo debe permitir la navegación interactiva por los siguientes flujos mediante un enrutador en JavaScript:

#### A) Flujo de Acceso (Público):
1. **Iniciar Sesión (Login):** Campos de Correo Institucional, Contraseña, botón de envío y un enlace "¿Olvidaste tu contraseña?".
2. **Registro:** Formulario con campos: Nombre Completo, Correo Institucional (debe terminar en @fte.edu.ec), Cédula de Identidad, Fecha de Nacimiento y Departamento. Al final, debe incluir una casilla o texto de aceptación de "Términos de Servicio y Políticas de Privacidad".
3. **Registro Exitoso (Success Splash):** Pantalla de confirmación con un check animado y un mensaje que indique que la cuenta está en espera de aprobación por parte del Administrador.

#### B) Portal del Estudiante (Privado):
1. **Dashboard de Estudiante:** Mensaje de bienvenida personalizado, tarjetas de cursos asignados con imagen de portada, indicador visual de progreso (%) y tag de estado ("Por hacer", "En curso", "Completado").
2. **Detalle de Curso:** Listado interactivo de módulos y temas organizados en formato de acordeón colapsable.
3. **Reproductor del Curso (Course Player):** Un visor dinámico con relación de aspecto 16:9 que cambia su contenido dependiendo del tema seleccionado en el acordeón de contenidos:
   - **Si es Video:** Muestra un reproductor de video simulado con barra de progreso interactiva y botones Play/Pause. Al hacer clic en Play, simula la reproducción y, tras 5 segundos de cuenta regresiva acelerada, muestra un check verde de éxito en el acordeón lateral del curso y actualiza el porcentaje global.
   - **Si es Práctica:** Presenta una instrucción (ej: realizar una fórmula condicional de Excel) y una caja de texto. Valida la fórmula escrita por el usuario (ej: `=SUMAR.SI(A1:A5; ">10")`) y muestra feedback animado de aprobación.
   - **Si es Evaluación (Quiz):** Muestra una portada con reglas y nota mínima (7.0/10.0), seguido de un cuestionario interactivo de 4 preguntas de opción múltiple, con botones de navegación anterior/siguiente, un indicador numérico de preguntas, y calificación instantánea.
4. **Pantallas de Resultados del Quiz:**
   - **Aprobado:** Muestra un velocímetro con la nota final (ej. 10/10), felicitaciones y un botón para ver/descargar el certificado institucional en una sección dedicada.
   - **Reprobado:** Muestra la nota insuficiente y un botón de reintento para reiniciar la evaluación.

#### C) Portal del Administrador (Privado):
1. **Gestión de Usuarios:** Tabla interactiva que lista colaboradores registrados, muestra su estado (activo/inactivo), y tiene un modal de formulario para agregar nuevos usuarios agregándose en tiempo real a la tabla.

#### D) Portal de Recursos Humanos (RRHH):
1. **Dashboard RRHH:** Vista analítica con KPIs y un gráfico dinámico (SVG) que se actualice animadamente para mostrar el avance de capacitación por departamento (Ventas, Finanzas, etc.) al aplicar filtros.

---

### 🕹️ 4. PANEL DE CONTROL DE PRUEBAS (DEVELOPER CONTROL PANEL)
Añade un menú flotante discreto (idealmente en la parte inferior o lateral) exclusivo del prototipo que permita:
1. Alternar instantáneamente el rol del usuario (Estudiante, Administrador, Recursos Humanos).
2. Saltar directamente a cualquier pantalla específica de la aplicación para agilizar las pruebas heurísticas y demostraciones.

Genera el código limpio y comentado repartido en tres archivos principales: `index.html` (estructura), `styles.css` (estilos premium responsivos) y `app.js` (toda la lógica interactiva SPA y simulación de base de datos local).

Link visible del primer prototipo de figma: https://www.figma.com/design/v82vYlmStcmeSvTplOtoWy/Sin-t%C3%ADtulo?node-id=0-1&t=d5fkzqTNhIBGmwwt-1
Link visible del segundo protipo mejorado https://www.figma.com/design/3iFVrnYqYlRbdYxwMiVITn/Sin-t%C3%ADtulo?node-id=0-1&t=zhqHOxZia3BtzBHp-1


