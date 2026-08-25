# EXCEDENTES

Sistema de cálculo y documentación de la Participación en las Ganancias del Personal, en el marco del Artículo 14 bis de la Constitución Nacional Argentina y la doctrina **La Cuarta Postura**.

## ¿Qué hace esta aplicación?

EXCEDENTES permite a una empresa:

1. Registrar sus **bienes de capital** (maquinaria, rodados, inmuebles) y calcular automáticamente su costo fijo anual (interés + amortización + mantenimiento + seguro + impuestos).
2. Registrar su **personal** (propio y de terceros) y su costo fijo anual (remuneración + cargas sociales).
3. Cargar los **datos financieros del ejercicio** (ventas, ganancia neta, retiros del titular).
4. Calcular la **distribución proporcional del excedente** entre capital y personal, según la proporción que cada uno representa sobre el costo fijo total de la empresa.
5. Generar un **reporte imprimible** con el detalle por trabajador, apto para fundamentar ante ARCA la solicitud de exención o reducción del Impuesto a las Ganancias, en los términos del RVPGE (Régimen Voluntario de Participación en las Ganancias del Personal) propuesto por La Cuarta Postura.
6. Exportar e importar los datos de cada empresa en formato `.json`, para guardar el trabajo y retomarlo después.

## Fundamento

El Art. 14 bis de la Constitución Nacional Argentina establece el derecho de los trabajadores a la "participación en las ganancias de las empresas" — un derecho vigente desde 1957 pero nunca reglamentado. Esta aplicación no reemplaza esa reglamentación (que es materia del proyecto de ley RVPGE), sino que ofrece a cualquier empresa una herramienta de cálculo para estimar, hoy, qué le correspondería a su personal bajo ese principio.

## Estructura de la app

La app se organiza en seis pasos secuenciales:

| Paso | Contenido |
|---|---|
| 01 — Empresa | Datos identificatorios del contribuyente |
| 02 — Capital | Bienes de capital y su costo fijo |
| 03 — Personal | Trabajadores propios y de terceros |
| 04 — Financiero | Ventas, ganancia neta y retiros del ejercicio |
| 05 — Resultado | Cálculo de la distribución, punto de equilibrio y proyección de aportes mensuales |
| 06 — Reporte | Documento final para presentación e impresión |

## Estado actual y limitaciones conocidas

- La sección "Distribución Anual" del Paso 05 ya refleja el mecanismo vigente de la doctrina: la empresa constituye mensualmente un fondo (Caja del Personal) y el reparto entre trabajadores se realiza una única vez al cierre del ejercicio, en proporción a lo percibido en sueldos durante ese período — no en la fecha de cumpleaños de cada trabajador.
- Los **cálculos internos** de esa misma sección (montos "por trabajador" y "por mes") todavía están construidos sobre la lógica anterior, de anticipos mensuales individuales. Producen una cifra de referencia útil, pero no reflejan aún con precisión el mecanismo colectivo de fondo único y reparto anual. Ajustar esa lógica de cálculo es una tarea pendiente.
- La constitución del fondo en dólares estadounidenses está sujeta a la normativa cambiaria vigente al momento de cada período — la app no valida ni advierte sobre restricciones al acceso a moneda extranjera.
- El cálculo no contempla todavía la contribución del 3% al sindicato con personería gremial, prevista en el articulado de la doctrina.

## Uso

La aplicación es un archivo `index.html` autocontenido (HTML, CSS y JavaScript en un solo archivo), sin dependencias de backend. Puede abrirse directamente en un navegador o publicarse como sitio estático (por ejemplo, vía GitHub Pages).

## Más información

- Doctrina completa: [cuartapostura.com](https://cuartapostura.com)
- Contacto: nestorgonzalezloza@gmail.com
