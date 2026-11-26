---
name: subir-cambios
description: "Revisa los cambios de un repositorio Git, prepara un commit y sube los cambios al remoto cuando el usuario pida subir, publicar o sincronizar cambios."
---

# Subir cambios

Usa esta skill cuando el usuario pida subir, publicar, sincronizar o hacer push de los cambios actuales del repositorio.

1. Inspecciona el repositorio con `git status --short --branch`, `git remote -v`, la rama actual y el último historial. Revisa el diff staged y unstaged suficiente para entender qué se va a subir.
2. Comprueba que no haya bloqueos evidentes antes de publicar: credenciales privadas, archivos generados grandes o cambios no relacionados. Las claves públicas de configuración web, como una clave de Firebase, no son por sí solas una razón para detenerse; verifica también que no se estén exponiendo secretos privados.
3. Si no hay cambios, informa de que el repositorio ya está limpio y no hagas commit vacío.
4. Si hay cambios, resume qué se va a publicar y pide confirmación explícita antes de cualquier `git commit` o `git push`, salvo que el usuario ya haya confirmado claramente esa acción en el mismo flujo.
5. Usa un mensaje de commit breve y descriptivo, respetando el idioma del usuario. No uses `git reset --hard`, `git checkout --` ni borres cambios del usuario.
6. Crea el commit y ejecuta `git push` hacia el remoto y la rama detectados. Si el push requiere permisos o autenticación, solicita la autorización necesaria y no intentes sortearla.
7. Verifica al final con `git status --short --branch` y `git log -1 --oneline --decorate`. Informa del hash del commit, remoto, rama y cualquier error restante.

No modifiques archivos de la aplicación como parte de esta skill. Si el usuario pide arreglar algo antes de subirlo, realiza primero ese trabajo y vuelve a revisar el diff.
