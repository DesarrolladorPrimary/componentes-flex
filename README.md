
# Guía completa de Flexbox en CSS aplicada al proyecto

Esta documentación te ayudará a entender y aplicar las propiedades más importantes de Flexbox, con ejemplos reales usados en este proyecto para organizar y alinear elementos web.

---



## 1. display: flex
Convierte un contenedor en un contexto flex, permitiendo usar todas las propiedades de Flexbox en sus hijos.

**Ejemplo real:**
```css
.top-nav {
  display: flex;
}
.menu-proyectos__nav {
  display: flex;
}
.nav-menu {
  display: flex;
}
.top-nav ul {
  display: flex;
}
```

---


## 2. flex-direction
Define la dirección principal en la que los elementos hijos se organizan dentro de un contenedor flex.

**Valores:**
- `row`: horizontal (izquierda a derecha)
- `row-reverse`: horizontal (derecha a izquierda)
- `column`: vertical (arriba a abajo)
- `column-reverse`: vertical (abajo a arriba)

**Ejemplo real:**
```css
.menu-proyectos__nav {
  flex-direction: column;
}
```

---


## 3. flex-wrap
Permite que los hijos se ajusten en varias líneas si no caben en una sola.

**Valores:**
- `nowrap`: todos los hijos en una sola línea (por defecto)
- `wrap`: los hijos se ajustan en varias líneas
- `wrap-reverse`: igual que wrap, pero en sentido inverso

**Ejemplo:**
```css
.contenedor {
  display: flex;
  flex-wrap: wrap;
}
```

---


## 4. flex-flow
Propiedad abreviada que combina `flex-direction` y `flex-wrap`.

**Sintaxis:**
```css
flex-flow: <flex-direction> <flex-wrap>;
```

**Ejemplo:**
```css
.contenedor {
  display: flex;
  flex-flow: column-reverse wrap;
}
```

---



## 5. justify-content
Alinea los elementos hijos a lo largo del eje principal del contenedor flex.

**Valores:**
- `flex-start`: al inicio del eje principal
- `flex-end`: al final del eje principal
- `center`: centrados en el eje principal
- `space-between`: espacio entre los hijos
- `space-around`: espacio alrededor de cada hijo
- `space-evenly`: espacio igual entre todos los hijos

**Ejemplo real:**
```css
.top-nav {
  justify-content: space-between;
}
.nav-menu {
  justify-content: start;
}
```

---



## 6. align-items
Alinea los elementos hijos a lo largo del eje secundario (por defecto, el eje vertical).

**Valores:**
- `stretch`: estira los hijos para llenar el contenedor (por defecto)
- `flex-start`: alinea los hijos al inicio del eje secundario
- `flex-end`: alinea los hijos al final del eje secundario
- `center`: centra los hijos en el eje secundario
- `baseline`: alinea los hijos según la línea base del texto

**Ejemplo real:**
```css
.top-nav {
  align-items: center;
}
.nav-menu {
  align-items: center;
}
.menu-proyectos__nav {
  align-items: center;
}
```

---


## 7. align-content
Alinea las líneas del contenedor flex cuando hay espacio extra en el eje secundario (solo funciona si hay varias líneas de hijos, es decir, si `flex-wrap` está activo).

**Valores:**
- `stretch`: estira las líneas para llenar el espacio (por defecto)
- `flex-start`: alinea las líneas al inicio del eje secundario
- `flex-end`: alinea las líneas al final del eje secundario
- `center`: centra las líneas en el eje secundario
- `space-between`: espacio entre las líneas
- `space-around`: espacio alrededor de cada línea
- `space-evenly`: espacio igual entre todas las líneas

**Ejemplo:**
```css
.contenedor {
  display: flex;
  flex-wrap: wrap;
  align-content: center;
}
```

---




## 8. gap
Establece el espacio entre los elementos hijos dentro de un contenedor flex, sin necesidad de usar márgenes individuales.

**Valores:**
- Cualquier unidad de medida CSS (`px`, `em`, `%`, etc.)

**Ejemplo:**
```css
.contenedor {
  display: flex;
  gap: 20px;
}
```

---

## 9. order
Permite cambiar el orden visual de los elementos hijos dentro de un contenedor flex, sin modificar el HTML.

**Valores:**
- Cualquier número entero (por defecto es 0)

**Ejemplo:**
```css
.hijo:nth-child(2) {
  order: 1;
}
.hijo:nth-child(3) {
  order: -1;
}
```

---

## 10. flex-grow
Permite que los elementos hijos crezcan para ocupar el espacio disponible en el contenedor flex.

**Valores:**
- Cualquier número (por defecto es 0)

**Ejemplo:**
```css
.hijo {
  flex-grow: 1;
}
```

---

## 11. flex-shrink
Define cuánto puede reducirse un elemento en relación a los demás cuando el espacio es insuficiente.

**Valores:**
- Cualquier número (por defecto es 1)

**Ejemplo:**
```css
.hijo {
  flex-shrink: 2;
}
```

---

## 12. flex-basis
Define el tamaño inicial de un elemento antes de que se distribuya el espacio restante.

**Valores:**
- Cualquier valor de tamaño CSS (`px`, `%`, `auto`, etc.)

**Ejemplo:**
```css
.hijo {
  flex-basis: 200px;
}
```

---

## 13. flex (shorthand)
Propiedad abreviada para `flex-grow`, `flex-shrink` y `flex-basis`.

**Sintaxis:**
```css
flex: <flex-grow> <flex-shrink> <flex-basis>;
```

**Ejemplo:**
```css
.hijo {
  flex: 1 0 150px;
}
```

---

## 14. align-self
Permite alinear individualmente un hijo dentro del contenedor flex, sobrescribiendo `align-items` solo para ese hijo.

**Valores:**
- `auto` (por defecto)
- `flex-start`
- `flex-end`
- `center`
- `baseline`
- `stretch`

**Ejemplo:**
```css
.hijo {
  align-self: flex-end;
}
```

---

## 15. place-content, place-items, place-self
Propiedades abreviadas para alinear contenido y elementos en ambos ejes (principal y secundario).

**Sintaxis:**
```css
place-content: center space-between;
place-items: start stretch;
place-self: end;
```

---

> **Tips avanzados:**
> - Usa `align-content` junto con `flex-wrap` para controlar la alineación de múltiples filas o columnas.
> - `gap` funciona tanto en Flexbox como en Grid y es la forma recomendada de espaciar elementos de manera uniforme.
> - Puedes anidar contenedores flex para layouts complejos.
> - Usa `min-width` y `max-width` junto con Flexbox para layouts responsivos.

---

¿Necesitas ejemplos visuales, explicación de otras propiedades de Flexbox o ayuda para adaptar Flexbox a tus propios componentes? ¡Pídelo!


---



> **Tip:** Usa `align-content` junto con `flex-wrap` para controlar la alineación de múltiples filas o columnas de elementos flex. Además, `gap` funciona tanto en Flexbox como en Grid y es la forma recomendada de espaciar elementos de manera uniforme.

---

¿Necesitas ejemplos visuales, explicación de otras propiedades de Flexbox o ayuda para adaptar Flexbox a tus propios componentes?
