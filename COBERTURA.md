# Cobertura de marcas

Qué marcas de casa inteligente maneja la app DoSync, cuáles se pueden sumar y cuáles
no, en **Norteamérica (NA)**, **Latinoamérica (LA)** y **Europa (EU)**. Se actualiza cada
vez que se agrega un adaptador.

*Brand coverage of the DoSync app across North America, Latin America and Europe,
updated every time an adapter is added.*

Última revisión: **9 de noviembre de 2026** (se sumaron MQTT genérico para proyectos caseros y las alarmas DSC con Envisalink; antes, los sensores, Hubitat, Homey, Tailwind, Awair, Enphase, Drayton Wiser y los avisos de cámaras Nest).

## Cómo leer la tabla

| Marca | Significado |
|---|---|
| ✅ | Funciona hoy. Entre paréntesis, cómo (red local, cuenta de la marca, infrarrojo). |
| 🟢 | Se puede sumar: tiene protocolo público o un emparejamiento legítimo. Pendiente nuestro. |
| 🟡 | Se puede sumar, pero hay que registrar DoSync en el portal de la marca. |
| ↪ | No tiene integración directa, pero funciona a través de Home Assistant, SmartThings, Matter o infrarrojo. |
| ⛔ | No se integra: la marca no ofrece forma pública y DoSync no usa claves sacadas de sus apps. |
| ❓ | Falta confirmar en qué plataforma corre (muchas marcas locales son Tuya con otro nombre). |

**Sobre las cifras.** Las cuotas de mercado por marca y por país no son públicas: están en
informes pagos (GfK/NIQ, Circana, IDC, Counterpoint). Este relevamiento se armó con lo que
sí es verificable: líderes por categoría según IDC y Counterpoint, las marcas que venden las
grandes cadenas y marketplaces (Home Depot, Mercado Libre, Fravega, Amazon) y la plataforma
técnica de cada marca. El orden dentro de cada categoría es por presencia, de mayor a menor.

## Resumen

- **Funcionan hoy:** 80 marcas o familias, más cientos de aires, teles y equipos por infrarrojo.
- **Sensores:** temperatura, humedad, CO₂, puerta, movimiento y agua desde Home Assistant,
  Zigbee2MQTT, ESPHome, SwitchBot, Netatmo y Bluetooth (BTHome / pvvx). Sirven para rutinas.
- **Proyectos caseros:** cualquier equipo que se anuncie por MQTT (Tasmota, ESPHome, Shelly,
  OpenMQTTGateway, Raspberry Pi o ESP32 propios), sin Home Assistant.
- **Alarmas:** DSC con Envisalink (armar, desarmar con confirmación y zonas). Risco, Paradox y
  Ajax no publican un protocolo: por Home Assistant o SmartThings.
- **Próximos sin trámite (🟢):** SolarEdge (por Modbus local: su API en la nube pone la clave
  en la dirección, y DoSync no manda claves así).
- **Con registro en el portal de la marca (🟡):** Home Connect, SmartThings sin vencimiento,
  TTLock, Honeywell Resideo, GE SmartHQ, Danfoss Ally y Google Home APIs.
- **Huecos que no se pueden cubrir directo:** Ring, Arlo, Blink, Wyze, Eufy, Ecovacs, Shark,
  Whirlpool, Haier/hOn, Midea por la nube, Hive, MyQ y Amazon Alexa.

---

## Luces y enchufes

| Marca | Región | Estado |
|---|---|---|
| Philips Hue | NA · LA · EU | ✅ (red local, con el puente) |
| Philips WiZ | NA · LA · EU | ✅ (red local) |
| TP-Link Kasa | NA · LA | ✅ (red local) |
| TP-Link Tapo | NA · LA · EU | ✅ (red local) |
| Smart Life / Tuya y sus marcas: Positivo, Nexxt, Steren, Feit, Nedis, Lidl Livarno, Ledvance WiFi | NA · LA · EU | ✅ (red local o cuenta Tuya) |
| Calex (luces, tiras LED y enchufes) | EU | ✅ (es Tuya: los aparatos se pasan de la app Calex Smart a Smart Life) |
| Govee | NA · EU | ✅ (red local o cuenta) |
| Xiaomi / Mi Home y Yeelight | LA · EU | ✅ (red local) |
| Shelly | EU · NA | ✅ (red local) |
| Sonoff / eWeLink (modo LAN) y Tasmota | LA · EU | ✅ (red local) |
| IKEA DIRIGERA | EU · NA | ✅ (red local) |
| LIFX, Nanoleaf, Elgato, WLED, Magic Home | NA · EU | ✅ (red local) |
| Belkin Wemo | NA | ✅ (red local) |
| Lutron Caséta Smart Bridge PRO y RA2 Select | NA | ✅ (red local, protocolo de integración oficial de Lutron) |
| Lutron Caséta con el puente común | NA | ↪ (SmartThings o Home Assistant) |
| Leviton, Eve | NA · EU | ↪ (Matter o SmartThings) |
| Innr, Osram/Ledvance Zigbee, Aqara | EU · LA | ↪ (Zigbee2MQTT, deCONZ, Matter) |
| Netzhome, Tecnolite Connect | LA (México) | ❓ |
| Intelbras Izy, Ekaza | LA (Brasil) | ❓ |
| Wyze, Meross, GE Cync | NA | ⛔ |

## Teles y video

| Marca | Región | Estado |
|---|---|---|
| Samsung | NA · LA · EU | ✅ (red local) |
| LG | NA · LA · EU | ✅ (red local) |
| TCL (Google TV o Roku TV) | NA · LA · EU | ✅ (red local) |
| Hisense con Google TV o Roku TV | NA · LA · EU | ✅ (red local) |
| Hisense con VIDAA | NA · LA · EU | ↪ (infrarrojo) · ⛔ por red |
| Sony Bravia | NA · LA · EU | ✅ (control por IP oficial de Sony; las que tienen Google TV, también como Android TV) |
| Philips | EU · LA | ✅ (red local) |
| Roku | NA · LA | ✅ (red local) |
| Amazon Fire TV y aparatos Android | NA · LA · EU | ✅ (ADB en la red local) |
| Chromecast / Google TV Streamer | NA · LA · EU | ✅ (red local) |
| Vizio | NA | ✅ (red local) |
| Panasonic (hasta 2018) | EU · LA | ✅ (red local) |
| Xiaomi, Sharp, Noblex, BGH y otras con Android TV | LA · EU | ✅ (red local) |
| Cualquier tele con control remoto | todas | ✅ (infrarrojo) |
| Apple TV | NA · EU | ⛔ |

## Audio

| Marca | Región | Estado |
|---|---|---|
| Sonos | NA · EU | ✅ (red local) |
| Bose SoundTouch | NA · EU | ✅ (red local) |
| Denon / Marantz / HEOS, Yamaha MusicCast, Onkyo / Pioneer | NA · EU | ✅ (red local) |
| Google Nest y parlantes con Google Cast (JBL, Sony) | NA · LA · EU | ✅ (red local) |
| Parlantes Bluetooth (LG XBOOM, JBL) | todas | ✅ (Bluetooth) |
| Amazon Echo, Apple HomePod | NA · LA · EU | ⛔ |

## Aires acondicionados y climatización

| Marca | Región | Estado |
|---|---|---|
| Cualquier aire con control remoto: BGH, Philco, Surrey, Carrier, Midea, Hisense, Mirage, Fujitsu, Hitachi | todas | ✅ (infrarrojo, biblioteca de cientos de modelos) |
| Hyundai (aires) | LA | ✅ (infrarrojo; **probado con un aire real** desde el emisor del celular, modelo HY6INV) |
| LG ThinQ | NA · LA · EU | ✅ (cuenta de la marca) |
| Samsung WindFree | NA · LA · EU | ✅ (SmartThings) |
| Daikin | EU · NA | ✅ (red local) |
| Gree | LA · EU | ✅ (red local) |
| Google Nest (termostatos) | NA · EU | ✅ (cuenta de la marca) |
| tado° | EU | ✅ (cuenta de la marca) |
| Netatmo / Legrand / BTicino | EU | ✅ (cuenta de la marca) |
| Bosch Smart Home, Homematic, FRITZ!DECT | EU | ✅ (red local) |
| Drayton Wiser | EU (Reino Unido) | ✅ (red local, con la clave del modo Setup del hub) |
| Honeywell / Resideo (Lyric, T-series) | NA · EU | 🟡 (programa de desarrolladores de Resideo) |
| Danfoss Ally | EU | 🟡 (API oficial con registro) |
| ecobee | NA | ↪ (Home Assistant; no da claves nuevas a desarrolladores) |
| BGH Smart Control, Mitsubishi (MELCloud, Kumo), Midea por la nube, Hisense ConnectLife, Fujitsu FGLair | todas | ↪ (infrarrojo) · ⛔ por la nube |
| Hive | EU (Reino Unido) | ⛔ |

## Electrodomésticos

| Marca | Región | Estado |
|---|---|---|
| Samsung | NA · LA · EU | ✅ (SmartThings) |
| LG ThinQ | NA · LA · EU | ✅ (cuenta de la marca) |
| Electrolux / AEG / Frigidaire | NA · LA · EU | ✅ (cuenta de la marca) |
| Miele | EU · NA | ✅ (cuenta de la marca) |
| Bosch / Siemens / Neff / Balay (Home Connect) | EU · NA · LA | 🟡 (registro en Home Connect) |
| GE Appliances (SmartHQ) | NA | 🟡 (programa de desarrolladores SmartHQ) |
| Aparatos sin conexión (microondas, cafetera) | todas | ✅ (enchufe inteligente) |
| Whirlpool, Haier / Candy (hOn), Midea | todas | ⛔ (↪ SmartThings si la marca lo permite) |

## Cerraduras y portones

| Marca | Región | Estado |
|---|---|---|
| Nuki | EU | ✅ (red local) |
| Tedee | EU | ✅ (red local) |
| SwitchBot | NA · EU | ✅ (cuenta de la marca) |
| Portones con ratgdo / ESPHome | NA | ✅ (red local) |
| Tailwind (portones) | NA | ✅ (red local) |
| TTLock y las cerraduras chinas que lo usan | LA · EU | 🟡 (registro en su plataforma abierta) |
| Yale / August, Schlage, Kwikset, Level | NA · EU | ↪ (Matter o Home Assistant) |
| Samsung (cerraduras SDS) | LA · NA | ↪ (SmartThings) |
| Intelbras | LA (Brasil) | ❓ |
| Chamberlain MyQ | NA | ⛔ |

## Cámaras

| Marca | Región | Estado |
|---|---|---|
| Hikvision, Dahua, Reolink, Amcrest, Imou, Ezviz y toda cámara ONVIF | todas | ✅ (red local: foto y **video en vivo** por RTSP; Imou Cruiser SE+ encontrada en una red real) |
| TP-Link Tapo (cámaras) | NA · LA · EU | ✅ (ONVIF en el puerto 2020, foto y video en vivo) |
| Google Nest (cámaras y timbres) | NA · EU | ✅ (avisos de movimiento, personas y timbre por Pub/Sub; sin fotos: la API solo da video en vivo) |
| Intelbras Mibo | LA (Brasil) | ❓ (ONVIF según el modelo) |
| Ring, Arlo, Blink, Wyze, Eufy | NA · EU | ⛔ |

## Aspiradoras robot

| Marca | Región | Estado |
|---|---|---|
| iRobot Roomba / Braava | NA · LA · EU | ✅ (red local) |
| Xiaomi, Roborock y Dreame vinculados a Mi Home | LA · EU · NA | ✅ (red local) |
| Roborock y Dreame con su propia app | todas | ⛔ (↪ Home Assistant) |
| Ecovacs, Shark, Eufy, Narwal | todas | ⛔ |

## Persianas y cortinas

| Marca | Región | Estado |
|---|---|---|
| Somfy TaHoma | EU · LA | ✅ (red local) |
| Hunter Douglas PowerView | NA · EU | ✅ (red local) |
| IKEA, SwitchBot Curtain | EU · NA | ✅ |
| Lutron Serena | NA | ✅ (con Smart Bridge PRO o RA2 Select) |

## Sensores (temperatura, humedad, CO₂, puerta, movimiento, agua)

Un sensor no se maneja: mide, y sus lecturas disparan rutinas ("si el baño pasa de 70 % de
humedad, prendé el extractor") o se consultan sin IA ("¿qué humedad hay en el baño?").

| Marca o fuente | Región | Estado |
|---|---|---|
| Cualquier sensor en Home Assistant (Zigbee, Z-Wave, Matter, Aqara, Sonoff…) | todas | ✅ (red local) |
| Cualquier sensor en Zigbee2MQTT (Aqara, Sonoff, Tuya Zigbee, IKEA…) | todas | ✅ (red local; al instante si el broker retiene los mensajes) |
| Placas ESPHome con sensores (DHT, BME280, SCD40, PIR, contacto) | todas | ✅ (red local) |
| SwitchBot Meter, Meter Plus, Meter Pro (CO₂), Outdoor, Hub 2, puerta, movimiento, agua | todas | ✅ (cuenta de la marca) |
| Netatmo estación meteorológica y Healthy Home Coach | EU · NA | ✅ (cuenta de la marca; si se conectó antes, volver a conectar) |
| Shelly BLU (puerta, movimiento, H&T) | todas | ✅ (Bluetooth, BTHome) |
| Termómetros Xiaomi LYWSD03MMC y similares con firmware pvvx o ATC | todas | ✅ (Bluetooth) |
| Termómetros Xiaomi con el firmware original | todas | ↪ (cifran con una clave de la nube de Xiaomi: por Home Assistant) |
| Shelly H&T y Door/Window por WiFi | todas | ↪ (duermen para ahorrar pila: por Home Assistant o MQTT) |
| Sensores Tuya / Smart Life | todas | ↪ (por Home Assistant o Zigbee2MQTT) |
| Awair (Element, Omni, Mint) | NA | ✅ (red local) |
| Hubitat y Homey: cualquier sensor que tengan | NA · EU | ✅ (red local) |
| Enphase: producción solar y consumo (W) | NA · EU | ✅ (red local) |
| Google Nest: movimiento en cámaras y timbres | NA · EU | ✅ (avisos por Pub/Sub) |

## Alarmas

Desarmar siempre espera la confirmación de una persona, venga la orden de donde venga.

| Marca | Región | Estado |
|---|---|---|
| DSC PowerSeries y Neo con Envisalink (EVL-3, EVL-4, UNO) | NA · LA | ✅ (red local, TPI publicado por Eyez-On) |
| Honeywell / Ademco Vista con Envisalink | NA | 🟢 (mismo módulo, otro dialecto del TPI) |
| Cualquier alarma en Home Assistant o SmartThings | todas | ↪ |
| Risco (LightSYS, Agility) | EU · LA | ↪ (sin protocolo publicado: por Home Assistant) |
| Paradox (IP150) | EU · LA | ↪ (sin protocolo publicado: por Home Assistant) |
| Ajax | EU · LA | ⛔ (sin API abierta) |
| Garnet, X-28 y otras centrales locales | LA (Argentina) | ❓ (falta confirmar si tienen interfaz documentada) |

## Proyectos caseros (Raspberry Pi, ESP32, MQTT)

| Fuente | Región | Estado |
|---|---|---|
| Cualquier equipo con descubrimiento MQTT (Tasmota, ESPHome, Shelly, OpenMQTTGateway, Frigate, scripts propios) | todas | ✅ (broker de la casa; luces, enchufes, persianas, cerraduras y sensores) |
| Placas ESPHome por su API nativa | todas | ✅ (red local) |
| Tasmota, WLED, Sonoff DIY por HTTP | todas | ✅ (red local) |
| Impresoras 3D con OctoPrint o Klipper | todas | ✅ (red local) |
| Raspberry Pi sin MQTT ni Home Assistant | todas | ↪ (publicar por MQTT con [descubrimiento](https://www.home-assistant.io/integrations/mqtt/#mqtt-discovery)) |

## Energía y calidad del aire

| Marca | Región | Estado |
|---|---|---|
| Shelly EM, enchufes con medición | todas | ✅ (red local) |
| Enphase (solar) | NA · EU | ✅ (red local, con el token de Enlighten) |
| SolarEdge (solar) | NA · EU | 🟢 (Modbus TCP local, SunSpec; la API en la nube lleva la clave en la dirección) |
| Awair (calidad del aire) | NA | ✅ (red local) |
| Rachio (riego) | NA | ✅ (cuenta de la marca) |
| Emporia, Sense | NA | ⛔ |

## Centrales y ecosistemas

| Marca | Región | Estado |
|---|---|---|
| Home Assistant | todas | ✅ (red local) |
| Samsung SmartThings | todas | ✅ (cuenta) · 🟡 para que el acceso no venza |
| Zigbee2MQTT, deCONZ, ESPHome, Homematic CCU | todas | ✅ (red local) |
| Matter | todas | ↪ (por Home Assistant) · 🟡 directo con Google Home APIs |
| Hubitat | NA | ✅ (red local, Maker API) |
| Homey Pro | EU | ✅ (red local, clave API) |
| Klipper / OctoPrint (impresoras 3D) | todas | ✅ (red local) |
| Apple Home, Amazon Alexa | todas | ⛔ (no tienen API para Android) |

---

## Fuentes consultadas

- Counterpoint Research, participación global de televisores (T1 2026): https://counterpointresearch.com/insights/global-tv-market-share
- Omdia, envíos de televisores T4 y crecimiento en Latinoamérica: https://www.pulse.bot/hardware/news/omdia-global-q4-tv-shipments-flat-despite-chinese-market-decline-b77d3d6d-41e4-4e5a-9740-caee6b919741
- Aspiradoras robot, concentración del mercado y datos de IDC: https://www.marketresearch.com/Prof-Research-v4036/Global-Robot-Vacuum-Cleaner-Consolidation-44817065/ · https://global.chinadaily.com.cn/a/202603/16/WS69b7361fa310d6866eb3deb7.html
- Europa, líderes de casa inteligente (Signify, Bosch, Legrand, Somfy): https://www.gminsights.com/industry-analysis/europe-smart-home-market
- Aires en Argentina (BGH, Philco, Surrey, TCL, Hisense): https://www.cronista.com/negocios/exploto-la-venta-de-aires-acondicionados-a-que-precios-se-consiguen-los-mas-demandados · https://mejorescompras.com.ar/mas-vendidos/mejores-aires-acondicionados-hot-sale-2026
- México, oferta de casa inteligente en Home Depot y tendencias de Tecnolite: https://www.homedepot.com.mx/s/inteligentE · https://cdn.uc.assets.prezly.com/305eb170-5672-404c-b394-a9c0e84644da/-/inline/no/Tecnolite_PR_Mayo2023_Hogares%20inteligentes%20TENDENCIA_V1%20(1).pdf
- Brasil, Positivo e Intelbras: https://www.tecmundo.com.br/produto/284446-tudo-voce-precisa-saber-comprar-artigos-inteligentes.htm · https://academia.nubimetrics.com/br/smart-home-produtos-em-alta-e-commerce
- Climatización en el Reino Unido (Hive, Resideo, Drayton Wiser): https://community.openhab.org/t/resideo-api-binding-for-honeywell-thermostats-and-sensors/159903 · https://community.home-assistant.io/t/recommended-a-heating-control-in-the-uk-for-ha/125725
- Aqara Hub M3 como puente Matter local: https://home-assistant.io/blog/2024/09/03/aqara-joins-works-with-home-assistant/
