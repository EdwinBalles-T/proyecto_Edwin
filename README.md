# Proyecto Final – Gestión de Versionamiento con Git y GitHub

Este proyecto consiste en la simulación completa de un flujo profesional de control de versiones utilizando Git y GitHub.
Incluye creación de ramas, manejo de issues, uso de tablero Kanban, generación y resolución de conflictos, Pull Requests y documentación detallada del proceso de trabajo.

# Objetivo del Proyecto
Aplicar un flujo de trabajo realista utilizando Git y GitHub, demostrando dominio de:
. Gestión de repositorios locales y remotos
. Colaboración mediante ramas (branching model)
. Manejo de issues y etiquetas
. Uso de tableros de proyecto (Kanban)
. Pull Requests y revisión de código
. Resolución de conflictos
. Documentación técnica del proceso

# Estructura del Proyecto
proyecto_Edwin/
│
├── index.html        # Página principal del proyecto web
├── style.css         # Estilos básicos del sitio
├── README.md         # Documentación general del proyecto
├── BITACORA.md       # Registro técnico detallado
└── evidencias/       # (opcional) Capturas de tablero, issues y PR

# Comandos de Git usados durante el proyecto
## Inicialización y configuración
git init
git config --global user.name "TuNombre"
git config --global user.email "tuemail@example.com"

## Estado, seguimiento y commits
git status
git add .
git commit -m "Mensaje de commit"

## Ramas (branching)
git branch nombre-rama
git checkout nombre-rama
git merge nombre-rama
git branch -d nombre-rama
git push origin --delete nombre-rama

## Trabajo con repositorio remoto
git remote add origin URL
git push --set-upstream origin main
git pull
git push

## Flujo de Git aplicado en el proyecto
El proyecto utilizó un flujo basado en ramas con tres ramas principales:
- feature/funcionalidad – desarrollo de nuevas características
- fix/correction – corrección de errores
- documentacion/docs – actualización y creación de documentación

## Flujo trabajado:
1. Crear una rama desde main
2. Realizar cambios locales
3. Agregar y confirmar cambios
4. Hacer push a GitHub
5. Crear un Pull Request
6. Revisar, aprobar y hacer merge en main
7. Eliminar ramas locales y remotas

## Conflicto generado y resuelto

Se generó un conflicto real en README.md editando la misma línea en GitHub y localmente.
El conflicto se resolvió manualmente y su explicación completa se encuentra en BITACORA.md.

## Pull Request realizado

Pull Request enviado al compañero para revisión: 
https://github.com/frankr0013/Proyecto-venus/pull/8




