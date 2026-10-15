# Catálogo de productos de Etiqueta Segura

Base de productos alimenticios vendidos en Argentina incluida en la app **Etiqueta Segura**.

## Origen y licencia

Los datos derivan de [Open Food Facts](https://world.openfoodfacts.org) (© Open Food Facts contributors) y se ofrecen bajo la
[Open Database License (ODbL) 1.0](https://opendatacommons.org/licenses/odbl/1-0/). El contenido individual de la base se rige por la
[Database Contents License](https://opendatacommons.org/licenses/dbcl/1-0/).

Podés usar, compartir y adaptar esta base respetando la ODbL: atribuir a Open Food Facts, indicar los cambios y compartir las
versiones adaptadas bajo la misma licencia.

## Modificaciones respecto del original

- Se filtraron productos con país Argentina y se conservaron solo los que tienen nombre y lista de ingredientes en español.
- Se descartaron productos cuya lista de ingredientes está mayormente en otros idiomas.
- Se descartaron valores nutricionales imposibles (por 100 g: más de 100 g de macronutrientes, más de 900 kcal, más de 40 000 mg
  de sodio) y los incoherentes (grasas saturadas mayores que las grasas totales, azúcares mayores que los carbohidratos).
- El sodio se expresa en mg por 100 g.
- Se agregó una categoría simplificada en español.

## Formato

`products.json`: lista de objetos con `id` (código de barras), `name`, `brand`, `ingredients`, `per100`
(`energy` en kcal; `protein`, `carbs`, `sugars`, `fat`, `satFat` y `fiber` en g; `sodium` en mg; todo por 100 g) y `category`.

## Aviso

Son datos colaborativos y pueden tener errores o estar desactualizados. No sustituyen la lectura del envase.
