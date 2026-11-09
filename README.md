# DoSync — catálogo de adaptadores

Catálogo público que usa la app **DoSync** para reconocer y controlar
dispositivos de la red local (luces, relés, televisores, cámaras, aires,
impresoras 3D…). La app lo descarga, verifica la firma y lo combina con la
copia que trae incluida, así que soporta marcas nuevas sin publicar otra
versión.

- Catálogo: [`catalog/v1/index.json`](catalog/v1/index.json)
- Firma Ed25519 del archivo exacto: [`catalog/v1/index.json.sig`](catalog/v1/index.json.sig)
- Servido en: https://giulianireg-spec.github.io/dosync-adapters/catalog/v1/index.json
- Política de privacidad de la app: https://giulianireg-spec.github.io/dosync-adapters/privacidad/
- **Qué marcas funcionan y cuáles vienen:** [COBERTURA.md](COBERTURA.md) (Norteamérica, Latinoamérica y Europa)

## Por qué es seguro descargarlo

Un adaptador es **un archivo de datos, no código**: describe cómo reconocer
un aparato y qué petición HTTP hace cada acción. Además:

1. **Firma**: la app solo acepta el catálogo si la firma coincide con la
   clave pública incluida en la app:

   ```
   74856b623508b8305a1b905a22a56a400f7ef8e8f85c94adba75670c2a0999cc
   ```

   Un catálogo alterado, firmado con otra clave o más viejo que el que la app
   ya tiene, se descarta.
2. **Límites del motor**, que la firma no puede saltarse: solo IPs de la red
   local (10.x, 172.16–31.x, 192.168.x), solo rutas (nunca otra URL), solo
   GET/POST/PUT, y las credenciales solo van al aparato que las entregó.

## Cómo se publica

Los adaptadores se escriben y prueban (cada uno con su simulador) en el
repositorio de la app, y se publican acá ya construidos y firmados con
`tools/publish-catalog.sh`. Los archivos de este repositorio no se editan a mano:
cualquier cambio invalidaría la firma.

## Códigos infrarrojos

[`ir/v1/`](ir/v1/) tiene códigos de controles remotos por marca y modelo
(aires acondicionados, teles y audio, ventiladores). La app baja el índice y,
cuando el usuario elige su modelo, solo ese archivo.

Los códigos vienen de [SmartIR](https://github.com/smartHomeHub/SmartIR),
© 2019 Vassilis Panos, bajo licencia MIT ([`ir/v1/LICENSE-SmartIR.txt`](ir/v1/LICENSE-SmartIR.txt)).
Se convirtieron con `tools/ir-library.ts` (solo los de formato Broadlink, y
cada código se verifica al convertir).
