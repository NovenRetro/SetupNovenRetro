# Setup NovenRetro
<p align="center">
  <img
    src="https://novenretro.github.io/SetupNovenRetro/logo-novenretro.png"
    alt="Setup NovenRetro"
    width="200">
  
</p>

## Descripción general

**Setup NovenRetro** es una herramienta basada en ESP32 para configurar tiras LED segmentadas a través de una interfaz web moderna y responsiva. Permite:
- Definir segmentos físicos de la tira LED.
- Ajustar color, brillo y efectos (Glow, Rainbow, Fire…).
- Guardar, cargar y eliminar hasta 5 presets con confirmaciones y reinicio automático.
- Descubrimiento en red vía mDNS (`<nombre>.local`) con nombre personalizable desde la web.
- Flasheo fácil desde navegador usando [https://novenretro.github.io/SetupNovenRetro/](https://novenretro.github.io/SetupNovenRetro/).

## Características principales

1. **Segmentación dinámica**  
   - Define nombre y longitud de cada segmento.
   - Visualiza suma de LEDs y punto de inicio de cada uno.

2. **Control de color y efectos**  
   - Color de tira y color de segmento con pickers HTML5.
   - Efectos:
     - **Glow** (ajustable en velocidad)
     - **Rainbow** y **Rainbow V2**
     - **Fire**

3. **Brillo y encendido**  
   - Rango de brillo 1–10.
   - Botón ON/OFF global.

4. **Presets**  
   - Hasta 5 presets guardables.
   - Guardar, cargar y eliminar con:
     - Mensajes de confirmación (alert/confirm).
     - Reinicio automático del ESP32 y recarga de la página.

5. **mDNS y nombre de dispositivo**  
   - Descubrimiento con `<nombre>.local` (por defecto `setup-novenretro.local`).  
   - Cambia el nombre desde **/config** → *Ruta del Dispositivo* sin recompilar.

6. **Flasheo desde web**  
   - Usa la página de flasheo:  
     `https://novenretro.github.io/SetupNovenRetro/`  
   - Conecta el ESP32 por USB, sigue las instrucciones y carga el firmware directamente desde el navegador.

## Requisitos

- ESP32 (Todos los chips compatibles)
- Tira de LEDs WS2812 / Neopixel
- Arduino IDE 1.8+ o PlatformIO
- Librerías:
  - `WiFi.h`
  - `WebServer.h`
  - `Adafruit_NeoPixel.h`
  - `Preferences.h`
  - `ImprovWiFiLibrary.h`
  - `ESPmDNS.h`

## Instalación y flasheo

1. **Desde Arduino IDE / PlatformIO**  
   - Clona este repositorio.
   - Selecciona tu placa ESP32.
   - Compila y sube.

2. **Flasheo web**  
   1. Abre [https://novenretro.github.io/SetupNovenRetro/](https://novenretro.github.io/SetupNovenRetro/).  
   2. Conecta tu ESP32 por USB.  
   3. Elige el puerto y firmware `.bin`.  
   4. Haz clic en **Flash** y espera al progreso.

## Uso

1. Conecta tu dispositivo a la red Wi-Fi (vía Improv o credenciales guardadas).
2. Accede a la IP o a `http://<nombre>.local` (por defecto `setup-novenretro.local`).
3. Define segmentos en **Configuración**.
4. Ajusta colores, efectos y brillo en la página principal.
5. Guarda tus presets y personaliza el nombre mDNS si lo deseas.


## Contribuir

¡Nos encantan las contribuciones!  
1. Haz un fork.  
2. Crea una rama: `feature/tu-mejora`.  
3. Envía tu pull request con descripción clara.

## Licencia

Este proyecto está bajo la [MIT License](LICENSE).  
© NovenRetro 2025 — Todos los derechos reservados.

---
**Web de flasheo y documentación** → https://novenretro.github.io/SetupNovenRetro/  
