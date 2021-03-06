## Clase: TouchBarScrubber

> Crear un depurador (un selector de desplazamiento)

Proceso: [Main](../tutorial/application-architecture.md#main-and-renderer-processes)

### `Nuevo depurador de la barra táctil(opciones)` *Experimental*

* `opciones` Object 
  * `elementos` [elemento a depurar[]](structures/scrubber-item.md) - Un arreglo de elementos a depurar.
  * `seleccionar` Función - llamado cuando el usuario toca un elemento que no era el último elemento tocado. 
    * `seleccionar índice` Entero - El índice del elemento que el usuario seleccionó.
  * `destacado` Función - llamado cuando el usuario toca cualquier elemento. 
    * `índice destacado` Entero - El índice del elemento que el usuario tocó.
  * `Seleccionar estilo` Cadena - Estilo del elemento seleccionado. Por defecto `nulo`.
  * `cubrir estilo` Cadena - Selecciona el estilo cubierto del elemento. Por defecto es `nulo`.
  * `Mostrar botones de flechas` Booleano - Por defecto es `falso`.
  * `modo` Cadena - Por defecto es `libre`.
  * `continuo` Booleano - Por defecto es `verdad`.

### Propiedades de Instancia

Las siguientes propiedades está disponibles en instancias del `depurador de barra tactil`:

#### `touchBarScrubber.items`

Un array de `ScrubberItem[]` representando los elementos en este depurador. Actualizar este valor actualiza inmediatamente el control en la barra táctil. Mientras se actualicen las propiedades profundas dentro de este arreglo **no se actualiza la barra táctil**.

#### `touchBarScrubber.selectedStyle`

Un `String` representando el estilo que deben tener los elementos en el depurador. Actualizar este valor inmediatamente actualiza el control en la barra táctil. Valores positivos:

* `background` - Mapa a `[NSScrubberSelectionStyle roundedBackgroundStyle]`.
* `outline` - Mapa a `[NSScrubberSelectionStyle outlineOverlayStyle]`.
* `null` - Actualiza nulo, no una cadena, remueve todos los estilos.

#### `touchBarScrubber.overlayStyle`

Una `Cadena` que representa el estilo que deben tener los elementos seleccionados por el depurador. Este estilo es cubierto en la parte superior del elemento depurador en vez de posicionarse detrás de él. Actualizar este valor inmediatamente actualiza el control en la barra de herramientas. Posibles valores:

* `background` - Mapa a `[NSScrubberSelectionStyle roundedBackgroundStyle]`.
* `outline` - Mapa a `[NSScrubberSelectionStyle outlineOverlayStyle]`.
* `null` - Actualiza nulo, no una cadena, remueve todos los estilos.

#### `touchBarScrubber.showArrowButtons`

Un `Booleano` representando si se muestran las flechas izquierda / derecha en el depurador. Actualizar este valor actualizará inmediatamente el control en la barra táctil.

#### `touchBarScrubber.mode`

Una `Cadena` representando el modo de este depurador. Actualizar este valor actualizará inmediatamente el control de la barra táctil. Valores posibles:

* `fijo` - Mapa a `NSScrubberModeFixed`.
* `libre` - Mapa a `NSScrubberModeFree`.

#### `touchBarScrubber.continuous`

Un `Booleano` representando si este depurador es continuo o no. Actualizar este valor actualizará inmediatamente el control en la barra táctil.