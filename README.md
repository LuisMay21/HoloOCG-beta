# HoloOCG (beta)

Simulador del **hololive OFFICIAL CARD GAME** con las reglas completas (Comprehensive Rules v1.9.0). Juegas contra la IA, contra otra persona en tu red local (LAN) o ves partidas IA contra IA. También puedes armar tus decks e importarlos de Deck Log o holoDelta. ¡Gracias por probarlo!

> Solo para Windows 10/11 de 64 bits.

---

## 1. Descargar

Entra a **[Releases](https://github.com/LuisMay21/HoloOCG-beta/releases)** y, en la versión más reciente, baja **uno** de estos dos archivos:

| Archivo | Para qué |
|---|---|
| **`HoloOCG-win-Setup.exe`** | Instalador (recomendado). Se instala solo y crea los accesos directos. |
| **`HoloOCG-win-Portable.zip`** | Versión portátil: la descomprimes en la carpeta que quieras, sin instalar nada. |

Los otros archivos (`.nupkg`, `RELEASES`, `.json`) son para las actualizaciones automáticas; no los necesitas.

## 2. Instalar

### Con el instalador
1. Abre `HoloOCG-win-Setup.exe`. No pide permisos de administrador.
2. Si sale **"Windows protegió tu PC"**, haz clic en **Más información → Ejecutar de todas formas**. Sale porque el juego todavía no tiene firma digital, no porque tenga algo malo.
3. Al terminar, el juego se abre solo.

**¿Dónde se instala?** En tu carpeta de usuario:

```
C:\Users\<tu usuario>\AppData\Local\HoloOCG
```

(puedes llegar ahí escribiendo `%LocalAppData%\HoloOCG` en la barra del Explorador de archivos).

**¿Quieres instalarlo en otra carpeta o disco?** El instalador no tiene esa ventana, pero puedes hacerlo de dos formas:
- **Desde una terminal** (PowerShell, en la carpeta donde bajaste el instalador):
  ```powershell
  .\HoloOCG-win-Setup.exe --installto "D:\Juegos\HoloOCG"
  ```
- **Con la versión portátil** (abajo).

### Con la versión portátil (ZIP, sin instalar)
Sirve si no quieres instalar nada, si quieres el juego en otro disco o en una USB.

1. Baja `HoloOCG-win-Portable.zip`.
2. **Antes de descomprimir, desbloquea el ZIP** (así Windows no marca cada archivo del juego como "descargado de internet"):
   clic derecho en el ZIP → **Propiedades** → abajo, en *Seguridad*, marca **Desbloquear** → **Aceptar**.
   (Si no aparece la casilla, ya está desbloqueado.)
3. Clic derecho en el ZIP → **Extraer todo...** → elige la carpeta (por ejemplo `D:\Juegos\HoloOCG`) → **Extraer**.
   Usa una carpeta tuya (Documentos, Escritorio, otro disco). **No** la pongas en `C:\Archivos de programa`: ahí el juego no puede actualizarse.
4. Dentro de esa carpeta verás:
   ```
   HoloOCG (beta).exe   <- ESTE es el que abres
   Update.exe           <- lo usa el juego para actualizarse; no lo borres
   current\             <- el juego en sí; no abras nada de aquí
   ```
5. Abre **`HoloOCG (beta).exe`**. Si quieres un acceso directo: clic derecho → **Enviar a → Escritorio (crear acceso directo)**.

No muevas ni borres `Update.exe` ni la carpeta `current`. Si quieres cambiar el juego de lugar, mueve **la carpeta completa**.

## 3. Abrir el juego

- **Instalado:** busca **"HoloOCG (beta)"** en el menú Inicio o usa el acceso directo del Escritorio.
- **Portátil:** abre `HoloOCG (beta).exe` en la carpeta donde lo descomprimiste.

La primera vez puede tardar unos segundos en abrir. El juego abre en pantalla completa; para cerrarlo usa el botón **"Salir"** del menú.

## 4. Si el juego no abre

Ve en orden; casi siempre es lo primero o lo segundo.

**a) Aviso azul "Windows protegió tu PC" (SmartScreen).**
Haz clic en **Más información → Ejecutar de todas formas**. Sale porque el juego todavía no tiene firma digital, no porque tenga algo malo. Solo sale la primera vez.

**b) Aviso "Parte de esta aplicación se ha bloqueado" (por ejemplo `HoloOCG.AI.dll`).**
Es el **Control inteligente de aplicaciones** (Smart App Control) de Windows 11: bloquea todo programa sin firma digital y **no** tiene botón para dejarlo pasar. Para poder jugar hay que apagarlo:

1. Abre **Configuración → Privacidad y seguridad → Seguridad de Windows**.
2. Entra a **Control de aplicaciones y navegador**.
3. En **Control inteligente de aplicaciones**, abre la configuración y elige **Desactivado**.
4. Abre el juego otra vez.

> ⚠️ **Importante:** una vez apagado, Windows **no deja volver a encenderlo** sin reinstalar o restablecer Windows. El antivirus (Microsoft Defender) y SmartScreen siguen protegiéndote igual. Si no quieres apagarlo, espera a una versión con firma digital.

**c) El antivirus borró o puso en cuarentena un archivo.**
Abre **Seguridad de Windows → Protección contra virus y amenazas → Historial de protección**, busca el archivo de HoloOCG y elige **Restaurar** / **Permitir en el dispositivo**. Después vuelve a instalar (o a extraer el ZIP). Si usas otro antivirus, agrega la carpeta del juego a sus excepciones.

**d) Abre y se cierra solo, o la pantalla queda negra.**
Actualiza el controlador de tu tarjeta de video (el juego necesita OpenGL 3.3, que tiene casi cualquier PC de los últimos 10 años). Si sigue igual, avísale al autor con tu modelo de PC.

**e) Usaste el ZIP y nada de lo anterior funciona.**
Borra la carpeta, vuelve a bajar el ZIP, **desbloquéalo** (paso 2 de la versión portátil) y extrae de nuevo.

## 5. Actualizaciones

Cuando haya una versión nueva, en el **menú del juego** aparece el botón **"Actualizar"**: el juego la descarga, se cierra y se abre ya actualizado. No necesitas volver a bajar nada de esta página (esto funciona en la versión instalada y en la portátil).

## 6. Cómo se juega

- En el menú eliges tu deck, el del rival y la dificultad (**Fácil**, **Normal** o **Difícil**). También puedes **ver IA contra IA**, en automático o paso a paso.
- Haz clic en una carta para ver su información y lo que puedes hacer con ella.
- **Arts:** haz clic en tu holomem del Center o de la Collab, elige el Art y luego el objetivo.
- **Bloom, equipar y Baton Pass:** elige la jugada en la carta y luego el objetivo resaltado.
- **Esc** o **clic derecho** cancela lo que no hayas confirmado. **Esc** también oculta las ventanas para ver el campo.
- **L** abre el registro, con la regla de cada paso.
- El botón **"Menu"** te regresa al menú (abandonando la partida). Al terminar una partida puedes volver al menú o salir del juego.

## 6b. Jugar contra otra persona (LAN)

Los dos tienen que estar en la **misma red** (la misma casa o el mismo Wi-Fi) y con **la misma versión** del juego.

1. Los dos van a **"Jugar en LAN"**, escriben su nombre y eligen su deck.
2. Uno pulsa **"Crear partida"**: el juego muestra su **IP** (por ejemplo `192.168.1.20`) y espera.
3. El otro pulsa **"Buscar partidas en la red local"** y elige la partida. Si no aparece, escribe la IP del primero y pulsa **"Unirse por IP"**.
4. Si se corta la conexión, la partida se **pausa 90 segundos** y quien se fue vuelve solo. La espera se puede cancelar. Si nadie vuelve a tiempo, o se cancela, es **doble derrota** (pierden los dos).
5. Al terminar cualquier partida, el juego pregunta si quieres **guardar la repetición** y te deja cambiarle el nombre.

### Si no se encuentran: permitir el juego en el firewall

La primera vez que creas una partida, Windows pregunta si HoloOCG puede usar la red: marca **"Redes privadas"** y pulsa **"Permitir acceso"**.

Si cerraste ese aviso o pusiste "Cancelar", **quien crea la partida** hace esto:

1. En **Inicio**, busca **"Permitir una aplicación a través del Firewall de Windows"** y ábrelo.
2. Pulsa **"Cambiar la configuración"**.
3. Busca **HoloOCG** en la lista y marca **"Privada"**. Si no está:
   - pulsa **"Permitir otra aplicación..." → "Examinar..."** y elige el `HoloOCG.exe` que está **dentro de la carpeta `current`**:
     - **Instalado:** `C:\Users\<tu usuario>\AppData\Local\HoloOCG\current\HoloOCG.exe`. Para llegar rápido, escribe `%LocalAppData%\HoloOCG\current` en la barra de direcciones.
     - **Portátil:** `<la carpeta donde lo descomprimiste>\current\HoloOCG.exe`.
   - pulsa **"Agregar"** y marca **"Privada"**.
4. Pulsa **"Aceptar"**.

**Con un comando (versión instalada):** abre PowerShell **como administrador** (clic derecho en Inicio → "Terminal (Administrador)") y pega:

```powershell
New-NetFirewallRule -DisplayName "HoloOCG (LAN)" -Direction Inbound -Program "$env:LOCALAPPDATA\HoloOCG\current\HoloOCG.exe" -Action Allow -Profile Private
```

(Para quitarlo después: `Remove-NetFirewallRule -DisplayName "HoloOCG (LAN)"`.)

**Tu red debe ser "privada":** Windows bloquea más en las redes públicas. Cámbialo en **Configuración → Red e Internet → Wi-Fi (o Ethernet) → tu red → Tipo de perfil de red: Privada**. En redes de escuelas, oficinas o cafés, la red suele impedir que dos equipos se vean, así que ahí el LAN puede no funcionar.

**Si el antivirus bloquea el juego:** agrega una exclusión para la carpeta del juego. En **Seguridad de Windows → Protección contra virus y amenazas → Administrar la configuración → Exclusiones → Agregar una exclusión → Carpeta**, elige `%LocalAppData%\HoloOCG` o la carpeta del portátil. Haz estas excepciones solo con el juego que bajaste de esta página.

## 7. Tus datos y desinstalar

- Tus partidas y repeticiones se guardan en `%AppData%\HoloOCG` (`C:\Users\<tu usuario>\AppData\Roaming\HoloOCG`).
- **Desinstalar (instalador):** Configuración → Aplicaciones → Aplicaciones instaladas → **HoloOCG (beta)** → Desinstalar.
- **Desinstalar (portátil):** borra la carpeta donde lo descomprimiste.
- En los dos casos, si también quieres borrar tus partidas, borra `%AppData%\HoloOCG`.

## 8. Reportar

Estamos en **fase de pruebas**: lo primero que se arregla es **el motor, las reglas y lo que no funciona**. Lo visual queda anotado para después, salvo que impida entender la partida.

Para reportar, entra a **[Issues → New issue](https://github.com/LuisMay21/HoloOCG-beta/issues/new/choose)** y elige el formulario:

- **Regla o carta mal aplicada:** una carta hizo algo distinto a su texto, o una regla se aplicó mal.
- **Algo no funciona:** se trabó, se cerró, no conecta, no guarda...
- **Sugerencia o detalle visual:** ideas para más adelante.

**Adjunta la repetición** si puedes, porque ayuda muchísimo. Al terminar la partida, el juego pregunta si quieres guardarla. Está en `%AppData%\HoloOCG\data\replays` (archivo `.hocgreplay`). GitHub no acepta esa extensión, así que **comprímela en un .zip** antes de subirla.

En la lista de [Issues](https://github.com/LuisMay21/HoloOCG-beta/issues) puedes ver lo que ya se reportó (así no se repite) y lo que ya se arregló.

---

*Proyecto de fans, sin fines de lucro. hololive OFFICIAL CARD GAME y las imágenes de las cartas son © COVER Corporation.*
