# Setup NovenRetro

<p align="center">
  <img
    src="https://novenretro.github.io/SetupNovenRetro/logo-novenretro.png"
    alt="Setup NovenRetro"
    width="200">
</p>

## Descripción general

**Setup NovenRetro** es una herramienta basada en ESP32 para configurar tiras LED segmentadas a través de una interfaz web moderna y responsiva.  

**Novedades hasta v2.0.x**  
- **OTA Update desde GitHub**  
  - Comprobación de `version.txt` en tu repositorio → botón **Buscar actualización** en `/config`  
  - Si hay nueva versión, se descarga e instala **automáticamente**  
  - Guarda la versión instalada en `Preferences` para futuras comparaciones  
- **Señalización post-arranque**  
  - Tras reinicio (incluyendo OTA) el LED azul de GPIO2 parpadea 3 s para indicar que el dispositivo está listo  
- **Hasta 10 presets** en lugar de 5  
- Personalización y refinamientos de UI (confirmaciones, alertas, recarga automática)

## Características principales

1. **Segmentación dinámica**  
   - Define nombre y longitud de cada segmento  
   - Visualiza la suma total de LEDs y el punto de inicio de cada segmento  

2. **Control de color y efectos**  
   - Color de tira y color de segmento con pickers HTML5  
   - Efectos disponibles:  
     - **Glow** (velocidad ajustable)  
     - **Rainbow** y **Rainbow V2**  
     - **Fire**

3. **Brillo y encendido**  
   - Rango de brillo 1–10  
   - Botón global ON/OFF

4. **Presets**  
   - Guarda hasta **10** configuraciones completas  
   - Guardar, cargar y eliminar con alert/confirm y reinicio automático del ESP32

5. **mDNS y nombre de dispositivo**  
   - Descubrimiento via `<nombre>.local` (por defecto `setup-novenretro.local`)  
   - Cambia el nombre desde **/config** sin recompilar

6. **Flasheo desde web**  
   - Abre [https://novenretro.github.io/SetupNovenRetro/](https://novenretro.github.io/SetupNovenRetro/)  
   - Conecta tu ESP32 por USB y selecciona el `.bin` para cargarlo directamente desde el navegador

7. **OTA directa**  
   - En `/config`, al pulsar **Buscar actualización**:
     - Si la versión en GitHub es más reciente que la guardada, se descarga e instala sin pedir confirmación manual.
     - Mensajes de estado: “Ya tienes la última versión…”, “Falló actualización: …”

8. **Indicador de arranque**  
   - El LED de GPIO2 parpadea 3 s al arrancar tras cualquier reinicio

## Requisitos

- ESP32 (Serie 32, WROOM, WROVER…)  
- Tira de LEDs WS2812 / NeoPixel  
- Arduino IDE 1.8+ o PlatformIO  
- Librerías:
  - `WiFi.h`
  - `WebServer.h`
  - `Adafruit_NeoPixel.h`
  - `Preferences.h`
  - `ImprovWiFiLibrary.h`
  - `ESPmDNS.h`
  - `HTTPClient.h`
  - `HTTPUpdate.h`

## Instalación y flasheo

### 1. Desde Arduino IDE / PlatformIO
1. Clona este repositorio.  
2. Selecciona tu placa ESP32.  
3. Compila y sube el firmware.

### 2. Flasheo web
1. Abre [https://novenretro.github.io/SetupNovenRetro/](https://novenretro.github.io/SetupNovenRetro/).  
2. Conecta tu ESP32 por USB.  
3. Elige el puerto y el firmware `.bin`.  
4. Haz clic en **Flash** y espera al progreso.

## Uso

1. Al arrancar, el LED azul (GPIO2) parpadea 3 s.  
2. Conecta vía ImprovWiFi o introduce tus credenciales Wi-Fi.  
3. Accede por IP o a `http://<nombre>.local` (por defecto `setup-novenretro.local`).  
4. En **Configuración**:  
   - Define tus segmentos físicos.  
   - Personaliza nombre mDNS, título y cabecera.  
5. En la página principal:  
   - Ajusta color, efectos y brillo.  
   - Usa ON/OFF y **Sorpréndeme** para selección aleatoria.  
6. **Presets**:  
   - Selecciona slot, pon nombre y guarda.  
   - Carga o elimina con confirmación.  
7. **OTA**:  
   - En `/config`, pulsa **Buscar actualización** (actualiza automáticamente si hay nueva versión).

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
