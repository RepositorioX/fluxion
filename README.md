![Fuxion logo](https://github.com/FluxionNetwork/fluxion/raw/master/logos/logo.jpg)

# Fluxion es el futuro de los ataques MITM WPA.
FFluxion es una herramienta de investigación en auditoría de seguridad e ingeniería social. Es una nueva versión de linset by vk496 con (con suerte) menos errores y más funcionalidad. El script intenta recuperar la clave WPA / WPA2 de un punto de acceso objetivo mediante un ataque de ingeniería social (phishing). Es compatible con la última versión de Kali (rodante). La configuración de los ataques de Fluxion es principalmente manual, pero el modo automático experimental maneja algunos de los parámetros de configuración de los ataques.  Lea las [preguntas frecuentes](https://github.com/FluxionNetwork/fluxion/wiki/FAQ) antes de solicitar problemas.

Si necesita ayuda rápida, fluxion también está disponible en gitter. Puedes hablar con nosotros en [Gitter](https://gitter.im/FluxionNetwork/Lobby) o en [Discord](https://discord.gg/G43gptk).
##  Instalación
Lea [aquí](https://github.com/FluxionNetwork/fluxion/wiki/Generate-ssh-keys) antes de hacer los siguientes pasos.
<br>
**Descarga la última revisión**
```
git clone git@github.com:FluxionNetwork/fluxion.git

# Cambiar al directorio de herramientas 

git clone https://www.github.com/FluxionNetwork/fluxion.git
```
**Ejecutar fluxion (las dependencias faltantes se instalarán automáticamente)**
```
cd fluxion 
```
**Run fluxion (missing dependencies will be auto-installed)**
```
./fluxion.sh
```

**Fluxion también está disponible en arch** 
```
cd bin/arch
makepkg
```

o usando el repositorio de Blackarch
```
pacman -S fluxion
```

## Registro de cambios
Fluxion recibe actualizaciones semanales con nuevas características, mejoras y correcciones de errores. Asegúrese de revisar el [registro de cambios aquí](https://github.com/FluxionNetwork/fluxion/commits/master).

##  Como contribuir
Todas las contribuciones son bienvenidas! Código, documentación, gráficos, o incluso sugerencias de diseño son bienvenidos; Usa GitHub al máximo. Envíe solicitudes de extracción, contribuya con tutoriales u otro contenido de la wiki. Sea lo que sea lo que tenga para ofrecer, se lo agradeceremos, pero siga la [guía de estilo](https://github.com/FluxionNetwork/fluxion/wiki/Code-style-guide).

## Cómo funciona
* Buscar una red inalámbrica de destino.
* Inicia el ataque Handshake Snooper .
* Capturar un apretón de manos (necesario para la verificación de contraseña).
* Lanzar ataque de Captive Portal .
* Genera un AP deshonesto (falso), imitando el punto de acceso original.
* Genera un servidor DNS, redirigiendo todas las solicitudes al host del atacante que ejecuta el portal cautivo.
* Crea un servidor web que sirve al portal cautivo que solicita a los usuarios su clave WPA / WPA2.
* Genera un jammer, autentificando a todos los clientes del AP original y atrayéndolos al AP deshonesto.
* Todos los intentos de autenticación en el portal cautivo se verifican con el archivo de reconocimiento que se capturó
  anteriormente.
* El ataque terminará automáticamente una vez que se haya enviado una clave correcta.
* La clave se registrará y los clientes podrán volver a conectarse al punto de acceso de destino.
* Para obtener una guía sobre el ataque del Captive Portal , lea la [guía de ataque del portal cautivo](https://github.com/FluxionNetwork/fluxion/wiki/Captive-Portal-Attack)

## Requerimientos

Un sistema operativo basado en Linux. Recomendamos Kali Linux 2018.4. Se recomienda una tarjeta wifi externa.

## Trabajo relacionado

FPara el desarrollo, uso vim y tmux. Aquí están mis [archivos dot](https://github.com/deltaxflux/takumi/)
## Creditos
1. l3op - contributor
2. dlinkproto - contributor
3. vk496 - developer of linset
4. Derv82 - @Wifite/2
5. Princeofguilty - @webpages and @buteforce
6. Photos for wiki @http://www.kalitutorials.net
7. Ons Ali @wallpaper
8. PappleTec @sites
9. MPX4132 - Fluxion V3

## Renuncia
* Los autores no son propietarios de los logotipos en el directorio /attacks/Captive Portal/sites/ . Exención de responsabilidad de derechos de autor Según la Sección 107 de la Ley de derechos de autor de 1976, se permite el "uso justo" para fines tales como críticas, comentarios, informes de noticias, enseñanza, becas e investigación.

* El uso de Fluxion para atacar infraestructuras sin el consentimiento mutuo previo podría considerarse una actividad ilegal y es altamente desalentador por parte de sus autores / desarrolladores. Es responsabilidad del usuario final obedecer todas las leyes locales, estatales y federales aplicables. Los autores no asumen ninguna responsabilidad y no son responsables de ningún uso indebido o daño causado por este programa.

## Nota
* Tenga cuidado con los sitios que simulen estar relacionados con el Proyecto Fluxion. Estos pueden estar entregando malware.

* Fluxion **NO FUNCIONA** en el subsistema Linux para Windows 10, porque el subsistema no permite el acceso a las interfaces de red. Cualquier problema relacionado con el mismo se ****cerrará inmediatamente**

## Links
**Fluxion website:** https://fluxionnetwork.github.io/fluxion/ <br>
**Discord:** https://discordapp.com/invite/G43gptk <br>
**Gitter:** https://gitter.im/FluxionNetwork/Lobby <br>
