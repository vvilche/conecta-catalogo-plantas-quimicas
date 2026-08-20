# Catálogo de Plantas Químicas Industriales — Chile

Catálogo HTML de plantas que fabrican compuestos químicos de proceso continuo en Chile
(cobre/azufre, agroquímicos, químicos industriales, minería, celulosa), como prospectos
CLIENTE FINAL para CONECTA Ingeniería (DCS SUPCON, SCADA, PMU/RTU, instrumentación).
Ángulo de venta: son plantas de proceso continuo → requieren DCS + instrumentación + SCADA.

## Estructura
- `index.html` — grid de tarjetas; cada tarjeta enlaza a su ficha.
- `ficha_<planta>.html` — ficha con 6 secciones: Quién es · Qué hace · Proyectos/clientes ·
  Tomadores de decisión (chips mailto/tel/LinkedIn) · Contacto corporativo · Ángulo CONECTA.
- `research/*.json` — datos crudos con fuentes verificables (origen de las fichas).
- `build/generate.py` — regenera index + fichas desde los JSON.

## Reglas de datos
- Nada se inventa: sin fuente pública verificable → campo vacío ("no verificado").
- Cada dato cita su URL de fuente (formato "↳ url").
- Prioridad a cargos TÉCNICOS (no solo gerente general).

## Rebuild
```bash
python3 build/generate.py
```
