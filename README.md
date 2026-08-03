# MasMoney

App de captura de finanzas personales. Funciona en el navegador, se instala en el teléfono
y guarda todo **en el dispositivo** — no hay servidor ni cuenta que crear.

**https://mascochicle.github.io/masmoney/**

Para instalarla: ábrela en Chrome → menú ⋮ → *Agregar a pantalla principal*.

## Qué hace

- Saldos de todas las cuentas: efectivo, bancos, tarjetas, créditos y activos.
- Las 7 operaciones de Money Pro: gasto, ingreso, transferencia, compra y venta de activo,
  adquisición y descarga de pasivo (esta última separa interés de capital).
- Multimoneda con tipo de cambio editable.
- En tarjetas: línea de crédito, uso con semáforo y próximo corte.
  En créditos: cuánto llevas pagado del total, con barra de avance.
- Calendario con los días que tienen movimientos, categorías y ámbitos editables,
  meses sin intereses, foto de la nota.

## Los datos

Viven en el `localStorage` del navegador y **no salen de ahí**. El respaldo es manual:
Ajustes → Exportar deja un `masmoney-AAAA-MM-DD.json` que conviene guardar en la nube.
Ese mismo archivo se carga con Importar.

Este repositorio contiene **solo el programa**: arranca sin ninguna cuenta y sin ningún
saldo. Los datos se cargan desde el respaldo la primera vez.

## Cómo se genera

El código fuente es un solo archivo. La versión publicada aquí se produce con
`masmoney_publicar.py`, que le quita el catálogo de cuentas de ejemplo y le agrega el
manifiesto, el service worker y los iconos.
