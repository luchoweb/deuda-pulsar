# Deuda Pulsar

Webapp estatica en Astro para controlar el cobro de una Pulsar NS 125 UG modelo 2026.

## Desarrollo

Requiere Node 22.12 o superior.

```bash
npm install
npm run dev
```

## Base de datos JSON

El archivo fuente esta en `/public/api/deuda-pulsar.json`.

Cada cuota tiene un arreglo `payments`. Para registrar un pago manual agrega objetos con este formato:

```json
{
  "date": "2026-06-20",
  "amount": 200000,
  "note": "Transferencia Bancolombia"
}
```

Puedes registrar varios pagos en una misma cuota si necesitas manejar abonos parciales.

## Despliegue en Netlify

- Build command: `npm run build`
- Publish directory: `dist`
- Redirect general incluido en `netlify.toml` y `public/_redirects`
