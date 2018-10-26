# ¿Cómo Contribuir?

Existen muchas formas en las que puedes contribuir a *la página web comunidad Python Barranquilla*.

Contribuyendo con código, escribiendo documentación, reportando errores, así
como leyendo y proporcionando tus comentarios a issues y pull-requests (PR),
todas son maneras necesarias y validas de ayudar.

Si deseas colaborar con código fuente, es importante tener en cuenta las
siguientes recomendaciones, que permitirán tener un control de los cambios que
se implementen y nos permita trabajar bajo los mismos lineamientos.

## Haciendo cambios en el código

Al ser *la página web comunidad Python Barranquilla* un proyecto abierto, todos pueden contribuir con sus cambios e
integrarlos al repositorio principal de una forma fácil.

Para esto recomendamos que todo el trabajo que hagas, lo realices en una rama
(branch) aparte. Cuando estés listo para trabajar en un error o en una nueva
característica, crea una rama (branch). La razón por la que esto es importante es
que puedes hacer tantos commits como consideres necesario. Cuando estés listo
puedes mezclarlos. Miremos como es el flujo básico:

    git checkout –b task-556
    … fix and git commit often …
    git push origin task-556

La razón por la que hemos creado dos ramas, es con el fin de mantenernos
alejados de la principal (master). Mantener la rama master limpia para los cambios
provenientes del repositorio principal (upstream) hace tu vida y la nuestra más
sencilla. Puedes enviarnos un pull request de tus cambios. Nosotros lo
revisaremos e integraremos al repositorio base.

Ten muy en cuenta los [Estilos de codificación](#Estilo-de-codificación), debido
a que pueden ser la causa de un rechazo a un pull-requests.

## Estilo de codificación

Cuando vayas a escribir código que quieras que sea incluido en *la página web comunidad Python Barranquilla*, ten
en cuenta el estilo de codificación que utilizas.

Estaremos validando que el código propuesto, cumpla con la mayoría de las reglas
definidas a continuación y en determinado momento, el no cumplir con estos
estilos puede generar un rechazo de tu PR.

> - Sigue los lineamientos del [PEP8][1]

## Issues

Puedes crear nuevos incidentes (issues) usando el botón "New issue" en la pestaña "Issues" del repositorio

![New Issue](./assets/img/contributing/new_issue.png)

Selecciona una de las plantillas según el tipo de incidente que deseas reportar presionando el respectivo botón "Get started"

![Issue templates](./assets/img/contributing/issue_templates.png)

Reemplaza el contenido de acuerdo a lo que quieres reportar reemplazando el texto por lo que se está solicitando

![Issue templates](./assets/img/contributing/issue_content.png)

## Pull Requests

Por favor mantén tus pull requests enfocados en un solo tema en específico.
Si tienes un número de solicitudes por enviar, entonces envía solicitudes
separadas. Es mucho más fácil recibir solicitudes pequeñas y bien definidas, que
tener que revisar y gestionar solicitudes grandes que apuntan a diferentes
temas.

Si terminas haciendo varios commits para un solo cambio (asociado a un tema
en particular), por favor, re-organízalo en un solo commit:

```sh
$ git rebase -i HEAD~10  # donde 10 es el número de commits que necesitas.
```

Esto abrirá un editor con tus  commits y algunas instrucciones que necesitas
seguir para poder escoger los commits que quieres integrar reemplazando ‘pick’
por ‘s’ para combinarlos con un commit previo.

Cuando guardes y salgas del editor donde estuviste combinando los commits, git
los combinará y te mostrará otro editor con los mensajes de commit. Escoge el
mensaje con el que quieres que quede el cambio (o escribe uno nuevo).
Guarda y sal para completar esta acción. Usa un push forzado a
tu repositorio (fork).

```sh
git push -f
```

Por favor asocia los pull request que hagas a los issues que estas resolviendo, preferiblemente usando la palabra 'closes' por ejemplo:

```bash
Closes #145
```

El cual [cierra][2] el issue #145 'Agregar Cierre automático de commits a contributing.md'

Para ver cual es el numero de issue asociado al caso que quieres resolver, lo encuentras debajo del titulo del ticket:

![El número que sale en gris debajo del titulo](./assets/img/contributing/issue_title.png)

Si quieres ver que otras palabras pueden cerrar automaticamente un issue (en ingles) ingresa al siguiente enlace: https://help.github.com/articles/closing-issues-using-keywords/ 

[1]: https://www.python.org/dev/peps/pep-0008/

[2]:
https://help.github.com/articles/closing-issues-using-keywords/
