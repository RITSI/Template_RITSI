# Template RITSI

Repositorio plantilla para nuevos proyectos y repositorios RITSI.

Utiliza este repositorio como plantilla para crear nuevos repositorios RITSI con la estructura y configuración básica, o bien, para realizar tus propios proyectos aprovechando las Github Actions que tenemos configuradas!

## Estructura

La estructura de este repositorio es la siguiente:

```
.
├── .github
│   ├── workflows
│   │   ├── auto-prerelease.yml
│   │   ├── auto-release.yml
│   │   ├── deploy-docs.yml
│   │   └── telegram-notify-issues.yml
│   ├── ISSUE_TEMPLATE
│   │   ├── bug_report.yml
│   │   ├── config.yml
│   │   ├── feature-request.yml
│   │   └── question.yml
```

## Configuración

### Github Actions

Para configurar las Github Actions, debes tener en cuenta que se van a utilizar las siguientes variables:

- `TELEGRAM_TOKEN`: Token de Telegram para el bot que enviará los mensajes. En la organización de RITSI está configurada como variable global, pero hay que habilitarla para el repositorio en cuestión.
- `TELEGRAM_TO`: ID de Telegram del usuario, canal o grupo al que se enviarán los mensajes. En la organización de RITSI está configurada como variable global, pero hay que habilitarla para el repositorio en cuestión. Cabe matizar que está puesto el identificador del canal de la Comisión.
- `TELEGRAM_TO_GROUP`: ID de Telegram del grupo al que se enviarán los mensajes. Esta variable se tiene que configurar en el repositorio en cuestión. Cabe matizar que se refiere al grupo de trabajo del repositorio en cuestión.

### Github Pages

Las Github Pages se tienen que configurar para que se desplieguen mediante las Github Actions. Para ello, hay que ir a la sección de `Settings` del repositorio, y en la sección de `Github Pages` seleccionar la opción de construir el sitio desde las Github Actions:

<!-- Imagen centrada -->
<p align="center">
  <img src="docs/images/gh_pages_config.png" alt="Github Pages" width="500"/>
</p>

### MkDocs

Para configurar MkDocs, se tiene que editar el archivo `mkdocs.yml` y cambiar el valor de la variable `site_name` por el nombre del repositorio. 



### Templates de issues

Las templates de las _issues_ se tendrán que revisar y configurar por cada repositorio para que se ajusten a las necesidades del mismo. Entre las necesidades más básicas podría estar el lengüaje de programación que se va a utilizar. 

## Cómo usar esta plantilla

Para usar esta plantilla, simplemente hay que hacer clic en el botón `Use this template` que aparece en la parte superior de este repositorio. Una vez hecho esto, se abrirá una ventana en la que se podrá configurar el nuevo repositorio. Una vez configurado, se creará el nuevo repositorio con la estructura y configuración básica.