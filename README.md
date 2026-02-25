# Apuntes-de-clase-U1

En este trabajo se presenta el desarrollo de una interfaz gráfica mediante Flet, un framework que facilita la creación de aplicaciones interactivas en Python de forma estructurada y compatible con múltiples plataformas. Durante el proceso se explicó cómo se diseña y organiza una interfaz gráfica, qué tipos de eventos permiten la interacción del usuario con la aplicación y de qué manera estos se gestionan a través de funciones que responden automáticamente a acciones como clics o modificaciones en campos de texto.
Además, se estudiaron los distintos componentes de control empleados en los programas desarrollados —entre ellos formularios, calculadoras y un sistema de chat—. Estos ejemplos permitieron comprender cómo se estructuran los elementos visuales, cómo recopilan información del usuario y cómo se integran con la lógica del programa para crear aplicaciones dinámicas y funcionales.

**La Interfaz Gráfica de Usuario** (GUI, por sus siglas en inglés) es el entorno visual de un sistema informático que utiliza iconos, menús, ventanas y punteros para permitir al usuario interactuar con aplicaciones y sistemas operativos. Sustituye los comandos de texto por manipulación directa, haciendo la tecnología más intuitiva, accesible y eficiente. 


Componentes y Características Clave:
Elementos Visuales (Widgets): Incluyen botones, barras de desplazamiento, iconos, menús desplegables y ventanas que permiten realizar acciones mediante un ratón o pantalla táctil.
WIMP: El modelo clásico se basa en Ventanas (Windows), Iconos (Icons), Menús (Menus) y Puntero (Pointer).
Interactividad: Permite una comunicación clara y directa, simplificando tareas complejas sin requerir conocimientos de programación. 

Importancia y Evolución:
Experiencia de Usuario (UX): Una GUI bien diseñada aumenta la usabilidad, fideliza a los usuarios y transmite la identidad de marca.
Origen: Popularizada en los años 80 por Apple (Lisa) y Microsoft (Windows 1.0) como evolución de la interfaz de línea de comandos.
Ejemplos: Entornos de escritorio (Windows, macOS, Linux), aplicaciones móviles y paneles táctiles de electrodomésticos. 

 
El desarrollo de una GUI es realizado por diseñadores de UI y desarrolladores frontend, enfocándose en la jerarquía visual, claridad y facilidad de uso

# 1.1 Creación de Interfaz Gráfica para Usuarios

Una **Interfaz Gráfica de Usuario (GUI)** es el medio visual con el que un usuario interactúa con un programa. Reemplaza los comandos de texto por elementos gráficos como ventanas, botones, menús y formularios.

## Objetivo principal
Permitir que el usuario controle el software de forma intuitiva, visual y amigable.

## Componentes principales de una GUI
- **Ventana (Window):** Contenedor principal.
- **Widget/Control:** Elemento interactivo (botón, texto, caja).
- **Layout o diseño:** Organización visual.
- **Estilos:** Colores, fuentes, bordes.
- **Eventos:** Acciones que produce el usuario.

## Herramientas populares para crear GUIs
| Lenguaje | Librería/Framework |
|---------|---------------------|
| Python | Tkinter, PyQt, Kivy |
| Java | Swing, JavaFX |
| C# | Windows Forms, WPF |
| C++ | Qt |
| JavaScript | Electron, Web GUI |

## Proceso para crear una GUI
1. Definir propósito del programa.
2. Identificar usuarios finales.
3. Diseñar la interfaz (bocetos).
4. Seleccionar framework o lenguaje.
5. Crear ventana principal.
6. Agregar componentes gráficos.
7. Programar eventos.
8. Probar usabilidad.

## Principios de diseño
- Consistencia visual.
- Retroalimentación clara al usuario.
- Accesibilidad (contraste, fuentes legibles).
- Minimizar pasos para realizar tareas.
- Alinear todos los elementos visuales.

# 1.2 Tipos de Eventos

Un **evento** es cualquier acción producida por el usuario o el sistema que debe ser procesada por la GUI.

Ejemplos: mover el mouse, escribir, hacer clic, cerrar ventana.

##  Clasificación principal de los eventos

###  1. Eventos del Mouse
- `click`
- `doble click`
- `mouse entered` (cursor entra a un área)
- `mouse exited` (cursor sale)
- `mouse pressed` / `released`
- `scroll` (rueda del ratón)

###  2. Eventos de Teclado
- `key pressed`
- `key released`
- `key typed`
- Detección de atajos: `Ctrl + C`, `Ctrl + S`

###  3. Eventos de Acción
Generados por botones u otros widgets de activación:
- `onClick` en un botón
- `onSelect` en un menú
- `submit` en formularios

###  4. Eventos de Ventana
- Abrir ventana
- Redimensionar
- Minimizar/maximizar
- Cerrar

###  5. Eventos del Sistema
- Cambios en red
- Notificaciones del sistema operativo
- Ticks de temporizadores

###  6. Eventos táctiles (móviles)
- Tap
- Swipe
- Long press
- Zoom

##  Por qué son importantes
Un programa con GUI funciona por eventos, no por un flujo secuencial.  
Es decir **el usuario controla la ejecución del programa**.

# 1.3 Manejo de Eventos

El **manejo de eventos** es el proceso mediante el cual un programa responde a acciones del usuario.

##  Objetivo
Detectar un evento → Ejecutar una función → Actualizar la interfaz.

##  Concepto clave: "Event Listener"
Un *listener* escucha continuamente eventos específicos.

Ejemplos:
- `button.onClick(function)`
- `window.onClose(handler)`
- `textbox.onKeyPress(callback)`

##  Flujo general del manejo de eventos
1. El usuario realiza una acción (clic, tecla…).
2. El sistema genera un evento.
3. El framework lo envía al programa.
4. La GUI verifica si hay un "listener" asociado.
5. Si existe, ejecuta la función correspondiente.
6. La interfaz se actualiza.

##  Técnicas comunes de manejo de eventos
- **Callbacks:** funciones llamadas cuando ocurre algo.
- **Funciones lambda:** permiten listeners rápidos.
- **Delegados (C#, Java):** patrones de asignación de eventos.
- **Event bubbling / capturing (JavaScript):** propagación del evento.

##  Buenas prácticas
- Mantener funciones de evento cortas y claras.
- Evitar lógica pesada en eventos.
- No bloquear la interfaz (usar *threads* o asincronía).
- Manejar errores silenciosos con mensajes claros al usuario.

# 1.4 Manejo de Componentes Gráficos de Control

Los **componentes gráficos de control** (widgets) son los elementos visuales que permiten la interacción entre el usuario y el sistema.

##  Tipos comunes de componentes

###  Botones
- Simples
- Toggle (encendido/apagado)
- Botones con iconos

###  Campos de texto
- Input de una línea
- TextArea
- Campo con placeholder
- Input con validación

###  Listas y tablas
- ListBox
- ComboBox (desplegable)
- Tablas dinámicas

###  Contenedores
- Paneles
- Frames
- Grid / Layouts

###  Barras
- Sliders
- ScrollBars
- ProgressBars

###  Otros
- Calendarios
- Selectores de color
- CheckBox
- RadioButton

##  Cómo manipular componentes
- Cambiar tamaño: `setSize()`
- Posición: `setPosition()`
- Texto: `setText()`
- Colores: `setColor()`
- Habilitar/deshabilitar: `setEnabled(false)`
- Mostrar/ocultar: `setVisible(true/false)`

##  Layouts o sistemas de diseño
Organizan los componentes dentro de la ventana.

Principales tipos:
- **Grid Layout** — rejilla.
- **Box Layout** — columnas o filas.
- **Flow Layout** — se acomodan según el espacio.
- **Absolute Layout** — posiciones fijas.

# Bibliografias

colaboradores de Wikipedia. (2026, 5 febrero). Interfaz gráfica de usuario. Wikipedia, la Enciclopedia Libre. https://es.wikipedia.org/wiki/Interfaz_gr%C3%A1fica_de_usuario 
https://sarreplec.caib.es/pluginfile.php/11696/mod_resource/content/2/323_tipos_de_eventos.htmlDe León Razo Jorge Alberto Solano Gálvez, T. I. A. R. A. N. C. J. A. (s. f.). Interfaz gráfica de usuario. Unidades de Apoyo Para el Aprendizaje - CUAED - UNAM. https://repositorio-uapa.cuaed.unam.mx/repositorio/moodle/pluginfile.php/3058/mod_resource/content/1/UAPA-Interfaz-Grafica-Usuario/index.html
