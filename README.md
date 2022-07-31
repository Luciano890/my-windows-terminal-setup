# My windows terminal setup

- [Finalizando](#Finalizando)

## Introducción

El presente repositorio es una guía básica para instalar mi configuración en la terminal de `Windows`, todos los archivos necesarios para la instalación de esta configuración estarán disponibles para su descarga mediante la clonación de este repositorio.

---

## Motivación

Obtener una configuración para la terminal de Windows que nos permita optimizar y elevar la productividad de los desarrolladores.

## Resultados

![ls](https://user-images.githubusercontent.com/62488915/182048778-33efa534-0d52-422a-bf5e-ee078c6a854f.png)

---

## ~~Instalación~~

~~Clonar el repositorio con el siguiente comando `git clone my-windows-terminal-setup@github.com`~~

---

## Primeros pasos

### Fuentes

Se deben instalar las fuentes necesarias para el correcto uso de la terminal, sobre todo por los temas que se configuraran más adelante en la terminal. En esta caso se hace uso de la fuente de letra `Hack Nerd Font` la cual se encuentra disponible en **Nerd Fonts** entre muchas otras, la url a este sitio es  [Nerd Fonts](https://www.nerdfonts.com "Nerd Fonts main page").

En el presente repositorio se encuentra un archivo `Hack.zip` que contiene las fuentes que se deben instalar para el correcto uso de la terminal, para ello se debe descomprimir el archivo y luego instalar las fuentes como se muestra en la imagen.

![instalacion-fuente-de-letra-hack](https://user-images.githubusercontent.com/62488915/182048857-308a2b58-9f2b-4bc0-a67a-dc93b419bef8.png)

### Instalación de la terminal

Vamos a instalar la terminal de Windows, para ello abrimos la Microsoft Store y buscamos la aplicación `Windows Terminal` y luego hacemos click en `Instalar`.

![store](https://user-images.githubusercontent.com/62488915/182048843-380cb2e0-8514-406a-853c-faccd4130cd2.png)

También instalaremos la última versión de `PowerShell` para que podamos usarla en la terminal.

![powershell](https://user-images.githubusercontent.com/62488915/182048921-3b877323-cd04-460d-ac24-c2215bacf5e6.png)

Dentro de la aplicación de Windows Terminal se encuentra una opción `Configuración` que nos permitirá configurar la terminal, en este caso seleccionaremos la opción de `Perfil predeterminado` y elegiremos **PowerShell**.

![defecto](https://user-images.githubusercontent.com/62488915/182048938-441d5479-d40c-4a9e-ba2c-ea8f38243186.png)

En la sección de `Apariencia` habilitaremos la opción de material acrílico para que la terminal sea mas atractiva y se vea mejor.

![acrilico](https://user-images.githubusercontent.com/62488915/182048955-c642eae3-94b7-46c1-9386-ddac971d64b6.png)

para guardar la configuración de la terminal seleccionamos la opción `Guardar` y luego reiniciamos la terminal.

De nuevo en la configuración de la terminal seleccionamos la opción `Valores predeterminados` y vamos a `Apariencia`.

#### Texto

* En la opción de `Combinación de colores` escogeremos **One Half Dark** (la cual más adelante modificaremos).

* En la opción de `Fuente de letra` seleccionaremos **Hack Nerd Font Mono**.

#### Transparencia

* En la opción de `Opacidad de fondo` seleccionaremos **35%** (puedes cambiarlo al gusto).

* Habilitaremos el material acrílico.

**Activar transparencia Windows**

> 👉 Si por algún motivo al activar la transparencia no se visualiza el fondo de la terminal, puedes leer el siguiente blog que explica posibles motivos [Activar Transparencia Windows](https://geekingup.org/es/corregir-el-efecto-de-transparencia-que-no-funciona-en-la-terminal-de-windows-en-windows-11 "Activar Transparencia Windows")

---

## Personalización

Dentro de la configuración de la terminal, en la parte inferior izquierda seleccionaremos la opción de `Abrir archivo JSON`

![json](https://user-images.githubusercontent.com/62488915/182048975-0f837356-0c26-4226-b78c-b2d7f4856908.png)

el cual desplegara un archivo *.json* que contiene la configuración de la terminal, el archivo se llama `settings.json`

> 👆 Puedes abrir este archivo con tu editor de texto/código favorito, por ejemplo, en Visual Studio Code.

> 👀 Mi configuración actual está en el archivo `settings.json`

> ⚠ No es recomendable copiar este archivo tal cual, del repositorio, es mejor seguir los pasos de manera manual.

### Modificación del tema

Buscamos la configuración del tema seleccionado para la combinación de colores, en este caso buscaremos `One Half Dark`, aparecerá una estructura de datos similar a la siguiente:

```json
{
    "background": "#282C34",
    "black": "#282C34",
    "blue": "#61AFEF",
    "brightBlack": "#5A6374",
    "brightBlue": "#61AFEF",
    "brightCyan": "#56B6C2",
    "brightGreen": "#98C379",
    "brightPurple": "#C678DD",
    "brightRed": "#E06C75",
    "brightWhite": "#DCDFE4",
    "brightYellow": "#E5C07B",
    "cursorColor": "#FFFFFF",
    "cyan": "#56B6C2",
    "foreground": "#DCDFE4",
    "green": "#98C379",
    "name": "One Half Dark",
    "purple": "#C678DD",
    "red": "#E06C75",
    "selectionBackground": "#FFFFFF",
    "white": "#DCDFE4",
    "yellow": "#E5C07B"
},
```

Podemos configurar los colores mediante esta estructura de datos, para ello seleccionaremos cualquier parámetro y después de `:` seleccionaremos el color que deseamos en formato hexadecimal.

### Creación de un nuevo tema

Para crear un nuevo tema a partir de una combinación preexistente, copiaremos la configuración y la pegaremos inmediatamente después de la última `,` siguiendo con la estructura de datos de arriba la estructura debe quedar de la siguiente manera.

```json
{
    "background": "#282C34",
    "black": "#282C34",
    "blue": "#61AFEF",
    "brightBlack": "#5A6374",
    "brightBlue": "#61AFEF",
    "brightCyan": "#56B6C2",
    "brightGreen": "#98C379",
    "brightPurple": "#C678DD",
    "brightRed": "#E06C75",
    "brightWhite": "#DCDFE4",
    "brightYellow": "#E5C07B",
    "cursorColor": "#FFFFFF",
    "cyan": "#56B6C2",
    "foreground": "#DCDFE4",
    "green": "#98C379",
    "name": "One Half Dark",
    "purple": "#C678DD",
    "red": "#E06C75",
    "selectionBackground": "#FFFFFF",
    "white": "#DCDFE4",
    "yellow": "#E5C07B"
},
{
    "background": "#001B26",
    "black": "#282C34",
    "blue": "#61AFEF",
    "brightBlack": "#5A6374",
    "brightBlue": "#61AFEF",
    "brightCyan": "#56B6C2",
    "brightGreen": "#98C379",
    "brightPurple": "#C678DD",
    "brightRed": "#E06C75",
    "brightWhite": "#DCDFE4",
    "brightYellow": "#E5C07B",
    "cursorColor": "#FFFFFF",
    "cyan": "#56B6C2",
    "foreground": "#DCDFE4",
    "green": "#98C379",
    "name": "One Half Dark (modded by LC)",
    "purple": "#C678DD",
    "red": "#E06C75",
    "selectionBackground": "#FFFFFF",
    "white": "#DCDFE4",
    "yellow": "#E5C07B"
}
```

Importante cambiar el nombre del tema, para ello seleccionaremos la opción `name` y después de `:` escribiremos el nombre del tema. En este caso:

```json
"name": "One Half Dark (modded by LC)"
```

Finalmente guardaremos la configuración, y dentro de las configuraciones de la terminal, seleccionaremos la opción del nuevo tema que acabamos de crear.

![nuevo_tema](https://user-images.githubusercontent.com/62488915/182048989-2486f858-ec57-4af1-b674-741d04504b5c.png)

---


## Programas

Descargaremos algunas aplicaciones que podemos usar en la terminal.

### Scoop

Para uso de un gestor de paquetes en la terminal usaremos `scoop`, en la terminal escribiremos el siguiente comando:

```bash
iwr -useb get.scoop.sh | iex
```

Esperamos que se instale el programa `scoop` en la terminal, y para confirmar que se instaló correctamente, podemos ejecutar el siguiente comando:

```bash
scoop --version
```

### Curl

Para peticiones del protocolo HTTP usaremos `curl`, mediante el gestor de paquetes de `scoop` podemos instalarlo.

```bash
scoop install curl sudo jq
```

Para confirmar el uso de `curl` ejecutamos el siguiente comando:

```bash
curl 'https://api.inkdrop.app/' | jq .
```

para observar 

```json
{
  "ok": true
}
```

### Git for Windows

No podemos olvidar el software de gestión de versiones, en este caso `git`, para ello podemos instalarlo mediante el siguiente comando:

```bash
winget install -e --id Git.Git
```

### NeoVim

Para el uso de un editor de texto en la terminal usaremos `neovim`, en la terminal escribiremos el siguiente comando:

```bash
scoop install neovim
```

y ejecutaremos el siguiente comando para observar el clásico mensaje de bienvenida de `neovim`:

```bash
nvim
```

---

## Creación de un perfil de usuario y configuracion de alias

En la terminal escribiremos el siguiente comando:

```bash
nvim .config/powershell/user_profile.ps1
```

El cual junto con `NeoVim` nos permitirá crear un perfil de usuario, y configurar alias para nuestra terminal. Escribiremos los siguientes comandos:

```bash
#Alias

Set-Alias vim nvim
Set-Alias ll ls
Set-Alias g git
Set-Alias grep findstr
Set-Alias tig 'C:\Program Files\Git\usr\bin\tig.exe'
Set-Alias less 'C:\Program Files\Git\usr\bin\less.exe'
```

El lector puede agregar más de un alias, para ello escribiremos la opción `Set-Alias` y después escribiremos el alias para luego escribir el comando que queremos que se ejecute.

* Guardaremos la configuración con: `:w`
* Volveremos a la terminal con: `:q`

Para que surta efecto en la terminal, debemos configurarlo para el perfil. Para ello escribiremos el siguiente comando:

```bash
nvim $PROFILE.CurrentUserCurrentHost
```

> 👆 En este archivo se guardará la configuración de Power Shell del perfil.

> ⚠ Si por algún motivo este archivo no está creado, podemos crearlo con el siguiente comando:

```bash
New-Item -Path $PROFILE -Type File -Force
```

Para luego escribir el siguiente comando dentro de esta configuración:

```bash
. $env:USERPROFILE\.config\powershell\user_profile.ps1
```

Eventualmente guardaremos la configuración con: `:wqa`, reiniciamos la terminal y comprobamos que los alias funcionen correctamente, ya sea con `ll` o `g`.

---

## Instalación de Oh My Posh

Oh my Posh es un framework para la terminal, que nos permite crear una configuración de terminal personalizada, muy similar a `Oh my Zsh` para Linux. Para instalarlo, escribiremos el siguiente comando:

```bash
winget install JanDeDobbeleer.OhMyPosh -s winget
```

Si queremos actualizar el framework, escribiremos el siguiente comando:

```bash
winget upgrade JanDeDobbeleer.OhMyPosh -s winget
```

Dentro de la configuración de `Power Shell`, escribiremos el siguiente comando:

```bash
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\paradox.omp.json" | Invoke-Expression
```

Esto es para configurar el tema de la terminal, en este caso `paradox`, que es el tema observado en `Resultados`.

---

## Plugins para la terminal

En este apartado instalaremos los plugins que nos permitirán usar la terminal de una manera mas productiva.

> 👆 Para activar algunos de estos plugins es necesario guardar con: `:wqa` y reiniciar la terminal.

### Terminal Icons

Este es un plugin que nos permite agregar iconos a la terminal, para ello escribiremos el siguiente comando (Se puede visualizar este plugin en acción en `Resultados`):

```bash
Install-Module -Name Terminal-Icons -Repository PSGallery -Force
```

Regresamos a `~./config/powershell/user_profile.ps1` y escribiremos el siguiente comando:

```bash
# Plugins
Import-Module -Name Terminal-Icons
```

luego del reinicio ahora escribiremos `ll` (alias para `ls`) y veremos los iconos de los directorios.

### Z - Directory Jumper

Este es un plugin que nos permite navegar entre los directorios de la terminal de una manera más ágil, para ello escribiremos el siguiente comando:

```bash
Install-Module -Name z -Force
```

Ahora escribiremos `z <nombre-directorio>` para guardar el atajo a este directorio.

![z](https://user-images.githubusercontent.com/62488915/182049026-935a09e7-7c96-4c25-accb-4d9341880df4.png)

### PSReadLine - Autocompletion

Este es un plugin que nos permite autocompletar los comandos de la terminal, para ello escribiremos el siguiente comando:

```bash
Install-Module -Name PSReadLine -AllowPrerelease -Scope CurrentUser -Force -SkipPublisherCheck
```

Para ver este plugin en acción, ejecutamos el siguiente comando:

```bash
Set-PSReadLineOption -PredictionSource History
```

Para observar una lista desplegable con el historial de comandos, escribiremos el siguiente comando:

```bash
Set-PSReadLineOption -PredictionViewStyle ListView
```

![history](https://user-images.githubusercontent.com/62488915/182049033-1428f545-d111-4875-ad24-9be69a53c224.png)

### Fzf - Fuzzy finder

Este es un plugin que nos permite buscar archivos en la terminal, para ello escribiremos el siguiente comando:

```bash
scoop install fzf
```

segudido de:

```bash
Install-Module -Name PSFzf -Scope CurrentUser -Force
```

Para configurar el plugin, escribiremos el siguiente comando:

```bash
Set-PsFzfOption -PSReadlineChordProvider 'Ctrl+f' -PSReadlineChordReverseHistory 'Ctrl+r'
```

Ahora con `Ctrl+f` desplegara una lista de archivos encontrados en el directorio actual, y `Ctrl+r` para observar el histórico de comandos.

![fzf](https://user-images.githubusercontent.com/62488915/182049048-5a80b096-4083-4e30-91b3-29a4d14a8eb2.png)

Regresamos a `~./config/powershell/user_profile.ps1` y escribiremos el siguiente comando:

```bash	
# Plugins
...
Import-Module PSFzf

# PSReadLine
Set-PSReadLineOption -EditMode Emacs
Set-PSReadLineOption -BellStyle None
Set-PSReadLineKeyHandler -Chord 'Ctrl+d' -Function DeleteChar
Set-PSReadLineOption -PredictionSource History
Set-PSReadLineOption -PredictionViewStyle ListView

# Fzf
Set-PsFzfOption -PSReadlineChordProvider 'Ctrl+f' -PSReadlineChordReverseHistory 'Ctrl+r'
```

### Git Aliases

Este es un plugin que nos permite agregar alias para git, para ello escribiremos el siguiente comando:

```bash
Install-Module git-aliases -Scope CurrentUser -AllowClobber
```

Regresamos a `~./config/powershell/user_profile.ps1` y escribiremos el siguiente comando:

```bash
# Plugins
...
Import-Module git-aliases -DisableNameChecking
```

> 👉 Para observar los alias de git, puede visitar el repositorio del plugin: [Git Aliases](https://github.com/gluons/powershell-git-aliases)

---

## Bonus Extra

### Activar Anaconda en la terminal 🐍

Abrir la terminal de `Anaconda` y escribir el siguiente comando:

```bash
conda init powershell
```

> 👉 Para más detalles, visitar el siguiente blog: [Anaconda en la terminal](https://hackf5.medium.com/how-to-enable-anaconda-in-powershell-7-on-windows-394ba62c3f9c)

Ahora `Anaconda` servirá en la terminal de `PowerShell`.

---

## Finalizando

¡Listo! Ahora podemos usar la terminal de `PowerShell` en la terminal de Windows para ser más productivos como desarrolladores, gracias por leer ✋.
