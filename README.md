# Catálogo de productos de Etiqueta Segura

Base de productos alimenticios vendidos en Argentina incluida en la app **Etiqueta Segura**.
Contiene **7,693 productos**: 4,466 con lista de ingredientes y 3,227 "parciales" (nombre, código y nutrición, sin ingredientes).

## Origen y licencia

Los datos derivan de [Open Food Facts](https://world.openfoodfacts.org) (© Open Food Facts contributors) y se ofrecen bajo la
[Open Database License (ODbL) 1.0](https://opendatacommons.org/licenses/odbl/1-0/). El contenido individual de la base se rige por la
[Database Contents License](https://opendatacommons.org/licenses/dbcl/1-0/).

Podés usar, compartir y adaptar esta base respetando la ODbL: atribuir a Open Food Facts, indicar los cambios y compartir las
versiones adaptadas bajo la misma licencia.

El campo `an` (519 productos) proviene de cruzar por marca y nombre con el listado **"Alimentos Libres de Gluten"** de la
Administración Nacional de Medicamentos, Alimentos y Tecnología Médica (ANMAT, Ministerio de Salud de la Nación), edición julio 2019,
publicado como dato abierto con licencia Creative Commons Atribución (CC BY) en
<https://datos.salud.gob.ar/dataset/alimentos-libres-de-gluten>. La coincidencia es por nombre y es solo informativa.

## Modificaciones respecto del original

- Se tomaron los productos con país Argentina (o código de barras argentino, prefijo 779) del volcado oficial de Open Food Facts.
- Se conservaron los que tienen nombre y lista de ingredientes en alfabeto latino; se descartaron los que están mayormente en idiomas que la app no interpreta.
- Se sacó de la lista de ingredientes el texto que no lo es (tabla nutricional, importador, lote…) solo cuando no se perdía ningún ingrediente.
- Se descartaron valores nutricionales imposibles (por 100 g: más de 100 g de macronutrientes, más de 900 kcal, más de 40 000 mg de sodio) y los incoherentes.
- El sodio se expresa en mg por 100 g.
- Se agregó una categoría simplificada en español.
- Se agregó el resultado del análisis de ingredientes de la app (`a`, `c`) y lo que Open Food Facts declara sobre alérgenos y origen animal (`o`).

## Formato

`products.json`: lista de objetos con
- `id` (código de barras), `name`, `brand`, `ingredients` (vacío en los parciales), `category`, `image` (foto en Open Food Facts, CC BY-SA, solo el enlace);
- `per100`: `energy` en kcal; `protein`, `carbs`, `sugars`, `fat`, `satFat` y `fiber` en g; `sodium` en mg; todo por 100 g;
- `a`, `c`: veredicto de ingredientes y propiedades nutricionales ya calculados por la app (máscaras de bits; no son datos de origen);
- `o`: alérgenos y "no vegano / no vegetariano" que declara Open Food Facts; `an`: figura en el listado ANMAT.

## Aviso

Son datos colaborativos y pueden tener errores o estar desactualizados. No sustituyen la lectura del envase.

## Productos que no son alimentos (`nonfood.json`)

Para la lista del súper, la app incluye además **515 productos de Argentina que no son alimentos** (higiene, hogar y limpieza, mascotas), 453 de ellos con foto, en `nonfood.json`.
Derivan de [Open Beauty Facts](https://world.openbeautyfacts.org), [Open Products Facts](https://world.openproductsfacts.org) y [Open Pet Food Facts](https://world.openpetfoodfacts.org)
(© sus colaboradores), bajo la misma [ODbL 1.0](https://opendatacommons.org/licenses/odbl/1-0/); las fotos de esos proyectos son CC BY-SA y se enlazan, no se copian.

Modificaciones: se tomaron los productos con país Argentina (o código de barras 779) y nombre; se descartaron tabaco, bebidas alcohólicas y los marcados como "tipo de producto incorrecto";
se simplificaron los campos a `c` (código), `n` (nombre), `b` (marca), `q` (cantidad), `g` (rubro) e `i` (dirección de la foto).
`nonfood_generic.json` es una lista de 259 sugerencias (genéricas y con marcas conocidas en Argentina; sin foto) escrita a mano para la app.
