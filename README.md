# Datos anuales de comercio exterior de Paraguay (DNIT)

Un Excel por año (2011–2026) y por operación (exportación e importación), armado con los datos abiertos
"Nivel Item" de la Dirección Nacional de Ingresos Tributarios (DNIT, https://datosabiertos.aduana.gov.py).

Cada archivo tiene: **Datos** (Calibri 10), **Descripciones** (texto de cada posición),
**Regímenes** (qué es cada código y si se cuenta) y **Notas**.

- Los meses se juntaron por año: se suman los ítems que coinciden en todos los campos de la DNIT, salvo los
  que cambian en cada despacho (número, fechas, mes, ítem, cotización, canal, mercadería y marca).
- No se filtró ningún régimen.
- **SE_CUENTA**: para sumar el comercio sin contar dos veces, filtrar SE_CUENTA = SI (solo regímenes
  definitivos). La mercadería que pasa por zona franca figura al entrar (NO) y al salir al país (SI).
- **MOTIVO_ARANCEL** (importaciones): con acuerdo, pagó arancel, AEC 0 %, o la lista de Paraguay notificada al
  MERCOSUR que explica el arancel cero (Bienes de Capital, Informática y Telecomunicaciones, Lista Nacional de
  Excepciones, Materias Primas); si no, otra ley o régimen nacional.
- Valores en dólares, salvo IMPONIBLE GS y los impuestos, en guaraníes. 2026: enero a octubre.

Código: `python/dnit_raw_por_anio.py` en
[comercio-exterior-paraguay-dnit-mic](https://github.com/silvia-mov/comercio-exterior-paraguay-dnit-mic).
Proyecto independiente; no representa a la DNIT.
