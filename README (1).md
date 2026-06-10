# Trakken Dashboard

Portal de clientes para Trakken Agency.

## Cómo agregar o editar clientes

Abre `index.html` y busca el bloque `const CLIENTS = [...]`.

Cada cliente tiene esta estructura:

```js
{
  id: 'id-unico',           // sin espacios, solo letras y guiones
  slug: 'url-del-cliente',  // aparece en el link que compartes
  name: 'Nombre de la clínica',
  specialty: 'Especialidad',
  avatar: 'XX',             // 2 letras que aparecen en el ícono
  pin: '1234',              // PIN de 4 dígitos del cliente
  status: 'meta',           // 'meta' | 'proceso' | 'bajo'
  metrics: {
    leads: 94,
    inv: '$1,200',
    cpl: '$12.77',
    roas: '3.2x',
    ag: 38,                 // agendados
    cag: '$31.58',          // costo por agendado
    msg: 127,               // mensajes
    fac: '$8,400',          // facturación
    cac: '$45.00',
    cmsg: '$9.45',          // costo por mensaje
    comp: 22,               // compras/cierres
    ccomp: '$54.54',        // costo por compra
    leadsD: '+18% vs anterior',
    roasD: '+0.4x',
    agD: '40% conversión',
    msgD: '$9.45/msg',
    facD: '+22%',
    compD: '23% cierre'
  },
  charts: {
    labels: ['Sem 1','Sem 2','Sem 3','Sem 4'],
    leads: [18,22,26,28],
    agendados: [7,9,11,11],
    cpl: [19,16,14,13],
    factura: [4200,5800,7100,8400],
    inversion: [1000,1100,1100,1200]
  }
}
```

## Deploy

1. Sube los archivos a GitHub
2. Conecta el repositorio en vercel.com
3. Click en Deploy — listo en 60 segundos

## Link por cliente

Cada cliente recibe:
`https://trakken-dashboard.vercel.app/cliente/[slug]`

El slug es el campo `slug` de cada cliente en el array CLIENTS.
