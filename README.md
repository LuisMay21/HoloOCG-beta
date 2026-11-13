# HoloOCG (beta)

Simulador del **hololive OFFICIAL CARD GAME** con las reglas completas (Comprehensive Rules v1.9.0). Juegas contra la IA o ves partidas IA contra IA. ¡Gracias por probarlo!

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

### Con la versión portátil
1. Descomprime `HoloOCG-win-Portable.zip` en la carpeta que quieras (por ejemplo `D:\Juegos\HoloOCG`).
2. Abre **`HoloOCG (beta).exe`** que está en esa carpeta. No abras los archivos de la carpeta `current`.

## 3. Abrir el juego

- **Instalado:** busca **"HoloOCG (beta)"** en el menú Inicio o usa el acceso directo del Escritorio.
- **Portátil:** abre `HoloOCG (beta).exe` en la carpeta donde lo descomprimiste.

## 4. Si Windows bloquea el juego ("Parte de esta aplicación se ha bloqueado")

Si te sale un aviso de **Seguridad de Windows** que dice que se bloqueó un archivo como `HoloOCG.AI.dll` porque *"no podemos confirmar quién lo publicó"*, es el **Control inteligente de aplicaciones** (Smart App Control) de Windows 11. Bloquea todo programa sin firma digital, y este aviso **no** tiene botón para dejarlo pasar.

Para poder jugar hay que apagarlo:

1. Abre **Configuración → Privacidad y seguridad → Seguridad de Windows**.
2. Entra a **Control de aplicaciones y navegador**.
3. En **Control inteligente de aplicaciones**, abre la configuración y elige **Desactivado**.
4. Abre el juego otra vez.

> ⚠️ **Importante:** una vez apagado, Windows **no deja volver a encenderlo** sin reinstalar o restablecer Windows. El antivirus (Microsoft Defender) y SmartScreen siguen protegiéndote igual. Si no quieres apagarlo, espera a una versión con firma digital.

Si solo te salió el aviso azul de "Windows protegió tu PC", no hace falta esto: basta con **Más información → Ejecutar de todas formas**.

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

## 7. Tus datos y desinstalar

- Tus partidas y repeticiones se guardan en `%AppData%\HoloOCG` (`C:\Users\<tu usuario>\AppData\Roaming\HoloOCG`).
- **Desinstalar (instalador):** Configuración → Aplicaciones → Aplicaciones instaladas → **HoloOCG (beta)** → Desinstalar.
- **Desinstalar (portátil):** borra la carpeta donde lo descomprimiste.
- En los dos casos, si también quieres borrar tus partidas, borra `%AppData%\HoloOCG`.

## 8. Reportar

Cuéntale al autor cualquier cosa rara, una regla que creas que está mal resuelta, o lo que te gustaría ver (animaciones, menús, opciones). Si puedes, incluye una captura de pantalla y el archivo de la partida de `%AppData%\HoloOCG`.

---

*Proyecto de fans, sin fines de lucro. hololive OFFICIAL CARD GAME y las imágenes de las cartas son © COVER Corporation.*
