# Guía Comenzando con Branches (Ramas) [![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)



Una **branch** (rama) en Git es una línea independiente de desarrollo que permite trabajar en **nuevas características**, corregir **errores** o **experimentar** con ideas sin afectar la rama principal del proyecto. 

Cada rama actúa como una **versión** separada del código, donde los desarrolladores pueden realizar **cambios y commits**. 

Las ramas facilitan la **colaboración** y la gestión del desarrollo paralelo, ya que permiten integrar los cambios de manera controlada mediante fusiones **(merges)**.

Al utilizar ramas, los equipos de desarrollo pueden mantener un flujo de trabajo **organizado** y minimizar los **conflictos** en el código.

## Tipos de Ramas 🌱

| Tipo  |  Descripción               |
| :-------- | :------------------------- |
| ![Master](https://i.imgur.com/c990QaN.png) | **Protected**. La rama principal del repositorio, donde se encuentra el código de producción estable. Todos los cambios en la rama master deben estar completamente probados y listos para ser desplegados. Es la base para crear nuevas ramas y la última versión oficial del proyecto. |
| ![Hotfix](https://i.imgur.com/Kup7h1I.png) | Creada a partir de la master para corregir rápidamente errores críticos en producción. Las hotfixes permiten solucionar problemas urgentes sin interrumpir el desarrollo en curso. Una vez que la corrección está lista, se fusiona de nuevo en master y, usualmente tambien en la rama de desarrollo para mantener la consistencia. |
| ![Development](https://i.imgur.com/c3jCeJQ.png) | Una rama donde se integran las características y mejoras que se están desarrollando. Es el entorno principal para la integración de cambios y pruebas antes de ser considerados estables y fusionados en la master. Funciona como un área de trabajo donde se realiza la mayor parte del desarrollo colaborativo. |
| ![Release](https://i.imgur.com/dcNmYqj.png) | Esta rama se crea a partir de la rama DEV-QAS cuando el proyecto está listo para una nueva versión **(tag)**. En esta rama, se realizan los últimos ajustes, pruebas y correcciones menores antes de lanzar la versión final. Una vez aprobada, se fusiona en master y se etiqueta con el número de versión. |
| ![Feature](https://i.imgur.com/VJPgCHL.png) | Ramas temporales creadas a partir de development para trabajar en nuevas funcionalidades o mejoras específicas. Cada feature branch se centra en una tarea particular y permite a los desarrolladores trabajar de manera aislada sin afectar el código base. Una vez completada y probada, la feature branch se fusiona de nuevo en development. |

## Comandos Imporantes a conocer 💻

Los comandos de Git relacionados con las ramas son fundamentales para gestionar el desarrollo de software de manera eficiente y colaborativa. Te permiten crear, cambiar, fusionar y eliminar ramas, facilitando el trabajo en múltiples funcionalidades, correcciones y versiones del proyecto simultáneamente.
Existen un centenar de aplicativos para reemplazar el uso de comandos, algunos particularmente muy buenos ya que para los usuarios "Windows" que estan acostumbrados a un entorno gráfico esto facilita enormemente la curva de aprendizaje GIT. De todas maneras es fundamental tener el conocimiento de que existen y para que se utilizan.

```bash
git branch
```
Este comando muestra el listado de ramas que se encuentran en el ambiente local y te marca con un * la rama en la cual actualmente estas trabajando.

```bash
git branch [branch-name]
```
Este comando permite crear una rama, ubicada en el commit que actualmente estas trabajando, es decir si se desea realizar una rama a partir de la **master** primero debes realizar un checkout a la rama master y luego ejecutar el comando.

```bash
git checkout [branch]
```
Este comando te permite cambiar a una rama que existe en el repositorio y crear una copia local de esa rama en tu ambiente de trabajo.

```bash
git merge [branch]
```
Uno de los comandos mas importantes, permite unir una rama especificada en el comando con la rama actual en la que te encuentras trabajando.

## Todo entra por la vista 👀

Como en varias ocaciones, uno aprende de una manera mas eficiente o atractiva utilizando imagenes, diagramas o contenido didactivo y no tan lineal. A continuación, se describe todo un flujo y uso de los distintos tipos de ramas que se presentaron anteriormente y los comandos.

![DiagramaGIT](https://i.imgur.com/RbO8sB4.png)

## Marco y Nomenclatura 📋

Como todo lenguaje de programación es importante tanto para el equipo de trabajo como para el dueño del código, que exista un orden, asi como en el código se debe comentar las principales funcionalidades, es imporante mantener una nomenclatura que sirva de cultura para tu equipo de trabajo es por eso que se indican a continuacion una serie de buenas prácticas.

### Branch

- Utiliza nombres claros precisos y que representen de manera general lo que aborda la rama.
- A pesar de que en GIT queda registrado el usuario que realizo la rama, que realizo el commit y todas sus modificaciones, es bueno tener un registro visual rápido de quien comenzo la rama, utiliza las iniciales del nombre y apellido.
- Identifica el tipo de rama para facilitar su seguimiento.

Con estos 3 pasos nos quedaria algo como el siguiente ejemplo:

```bash
CA-HF-REPARA_BOTON_MODULO_A
```

```bash
CA-F-MODULO_B
```

```bash
CA-R-MODULO_B
```

### TAG's

Los Tags permiten etiquetar una versión del código que representa un punto estable en el tiempo, tras aplicar un Release oficial de un desarrollo nuevo.

```bash
NOMBRE_SISTEMA_V1.0
```
En caso de que exista un hotfix entre una Feature y otra, esta se puede etiquetar como una versión nueva dentro del mismo punto.
```bash
NOMBRE_SISTEMA_V1.1
```
Otra forma de representar un tag es identificando de manera clara la fecha, codificandola para que se ordenen de forma incremental.
```bash
NOMBRE_SISTEMA_V1.20240524
```

## Metodología 

Para todo proyecto es bueno contar con una metodología de trabajo, usar metodologías ágiles con KANBAN en el desarrollo con Git es altamente beneficioso porque proporciona una estructura **visual** clara para **gestionar** y priorizar tareas, facilitando la colaboración y la entrega continua.

KANBAN permite a los equipos visualizar el flujo de trabajo a través de tableros, identificar cuellos de botella y mejorar la eficiencia en el desarrollo. 

Integrado con Git, KANBAN ayuda a sincronizar las ramas y commits con las tareas específicas, asegurando que cada cambio en el código está alineado con los objetivos y prioridades del proyecto. 

Esta combinación mejora la transparencia, la comunicación y la capacidad de adaptación a cambios, lo que resulta en un desarrollo más ágil y eficaz.

Ejemplo usando Trello:
![Trello](https://i.imgur.com/miqg9jf.png)

Ejemplo de una tarjeta Trello integrada con Github:
![Trello-Card](https://i.imgur.com/3buUdUY.png)

# Links de utilidad

- [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)
- [Trello](https://trello.com/)

# Author

[@carlosaravena](https://github.com/carlosaravena)
