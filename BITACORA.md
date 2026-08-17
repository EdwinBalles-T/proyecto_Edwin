# BITÁCORA DEL PROYECTO – Gestión de Versionamiento con Git y GitHub

Este documento registra todos los procesos técnicos realizados durante el proyecto: configuración, creación de ramas, flujo de trabajo, conflictos, uso de Pull Requests, diferencias entre comandos y aprendizajes clave.

# 1. Configuración de Git: Global vs Local

## Configuración global

Se aplica a todos los repositorios del equipo.
Esta configuración define la identidad del usuario en cualquier proyecto Git del sistema.

git config --global user.name "TuNombre"
git config --global user.email "tuemail@example.com"

Se usa cuando un mismo usuario trabaja en varios proyectos desde la misma máquina.

## Configuración local

Solo afecta al repositorio actual.
Se aplica cuando se requiere un nombre o correo distinto por proyecto.

git config user.name "NombreProyecto"
git config user.email "correo@proyecto.com"

# 2. Justificación y uso de ramas (branching)

El proyecto utilizó un modelo de trabajo basado en ramas para separar tareas y evitar conflictos en main.

## Ramas creadas
. feature/funcionalidad → para agregar nuevas funciones
. fix/correction → para corregir errores
. documentacion/docs → para actualizar documentación

## ¿Por qué usar ramas?
. Permite trabajar de forma paralela sin afectar la versión estable.
. Facilita revisiones mediante Pull Requests.
. Reduce riesgos de errores en producción.
. Permite revertir cambios sin comprometer el proyecto completo.

# 3. Descripción del conflicto generado

Para demostrar manejo de conflictos, se editó la misma línea del archivo README.md en:

. El repositorio local
. El repositorio remoto (GitHub)

## Contenido local añadido:
conflicto local

## Contenido remoto añadido:
Generacion de conflicto remoto

Al ejecutar:

git pull

Git detectó que el archivo tenía diferencias irreconciliables automáticamente y generó un conflicto.

El archivo mostró marcadores como:
---------------------------------------------------------
| <<<<<<< HEAD                                          |
| conflicto local                                       |
| =======                                               |
| Generacion de conflicto remoto                        |
| >>>>>>> b7b41cdfb24b5553de4c3e914a8a5114741d0645      |
---------------------------------------------------------
# 4. Resolución del conflicto

El conflicto se resolvió manualmente reemplazando todo por la versión final deseada:

Proyecto GIT - README (edición LOCAL y REMOTA)


Luego:

git add README.md
git commit -m "Conflicto resuelto en README.md"


Este proceso se registró para demostrar manejo de colaboración y control de versiones.

# 📌 5. Diferencia entre reset y revert
## 🛑 git reset

. Modifica el historial de commits.
. Puede borrar commits permanentemente.
. No debe usarse en repositorios compartidos.

Ejemplo:

git reset --hard HEAD~1

## git revert

. Crea un nuevo commit que deshace un commit anterior.
. No borra historial.
. Seguro para repositorios remotos y trabajo colaborativo.

Ejemplo:

git revert ID_DEL_COMMIT

Conclusión:

reset = reescribe historia → peligro en equipo
revert = deshace sin eliminar → recomendado

# 6. Explicación del fork

Un fork es una copia completa de un repositorio que pasa a ser propiedad del usuario.
Se usa cuando se quiere contribuir a repositorios que no te pertenecen.

Permite:

. Modificar sin afectar al original
. Enviar Pull Requests para colaborar
. Practicar sobre código real

En el proyecto se hizo un fork del repositorio del compañero para enviar un Pull Request.

 7. Detalles del Pull Request enviado

Se realizó un Pull Request hacia el repositorio del compañero:

 https://github.com/frankr0013/Proyecto-venus/pull/8

Este PR permitió:

. Simular revisión de código entre pares
. Usar el flujo de colaboración en GitHub
. Aplicar buenas prácticas de versionamiento

# 8. Uso del tablero Kanban e Issues

En GitHub Projects se creó un tablero con columnas:

. To Do
. In Progress
. Done

Los issues creados se movieron por el flujo conforme se avanzaba en su desarrollo.
Esto permitió visualizar:

. Trabajo pendiente
. Progreso en tiempo real
. Tareas finalizadas

El uso del tablero simuló un entorno real de gestión de proyectos.

# 9. Aprendizajes clave

. Git permite controlar versiones de manera estructurada.
. Las ramas facilitan organización y trabajo colaborativo.
. Los conflictos son normales y parte del proceso profesional.
. GitHub Projects mejora la visualización del flujo de trabajo.
. Pull Requests permiten revisión y aseguramiento de calidad.
. Saber resolver conflictos es una habilidad esencial.
