# Examen práctico de Front-End

## Manipulación del DOM y renderizado dinámico de datos

---

## Información general

* **Duración máxima:** 3 horas
* **Modalidad:** Individual
* **Tecnologías permitidas:**

  * HTML5
  * CSS3
  * JavaScript
  * Herramientas de inteligencia artificial generativa
* **Entrega:** Repositorio de GitHub
* **Tema principal:** Manipulación del DOM y carga dinámica de información
* **Valor:** 100 puntos
* **Puntos adicionales:** Hasta 10 puntos

---

# Caso empresarial

## TechStore: catálogo digital de productos tecnológicos

La empresa **TechStore** comercializa productos tecnológicos como computadores, periféricos, dispositivos móviles, accesorios y componentes.

Actualmente, la empresa administra su inventario mediante documentos y hojas de cálculo. Esta situación dificulta la consulta rápida de los productos disponibles y la presentación organizada de la información.

La empresa requiere una aplicación web que permita visualizar su catálogo de productos de forma dinámica.

Para resolver esta necesidad, deberás desarrollar una interfaz web utilizando **HTML, CSS y JavaScript**, en la cual se cargue un conjunto de productos almacenados en formato JSON.

La información no debe escribirse directamente en el HTML. Todos los productos deberán generarse y mostrarse dinámicamente utilizando JavaScript y manipulación del DOM.

---

# Objetivo del examen

Construir una aplicación web que permita:

1. Presentar información general de la empresa.
2. Cargar un conjunto de 50 productos desde un arreglo de objetos JSON.
3. Recorrer el arreglo utilizando JavaScript.
4. Crear elementos HTML dinámicamente.
5. Mostrar los productos en una tabla o en un sistema de tarjetas.
6. Aplicar estilos CSS para construir una interfaz clara, organizada y funcional.
7. Implementar al menos una interacción utilizando eventos del DOM.

---

# Requerimientos

## 1. Estructura del proyecto

El proyecto deberá contener como mínimo la siguiente estructura:

```text
techstore/
│
├── index.html
├── css/
│   └── styles.css
├── js/
│   └── app.js
├── data/
│   └── productos.js
├── img/
│   └── recursos-del-proyecto
└── README.md
```

También se permite utilizar una estructura diferente, siempre que los archivos estén organizados correctamente.

---

## 2. Interfaz gráfica

La aplicación deberá incluir como mínimo las siguientes secciones:

### Encabezado

Debe contener:

* Nombre de la empresa.
* Logotipo, ícono o elemento visual relacionado.
* Título del catálogo.
* Menú de navegación básico o enlaces internos.

### Sección principal

Debe contener:

* Una descripción breve de la empresa.
* Un título para el catálogo.
* Un contador que indique la cantidad de productos cargados.
* Un espacio donde se mostrarán dinámicamente los productos.

### Pie de página

Debe contener:

* Nombre del estudiante.
* Grupo.
* Año.
* Nombre de la institución o programa académico.

---

## 3. Creación del conjunto de datos

Utiliza un agente de inteligencia artificial para generar un arreglo JSON con exactamente **50 productos tecnológicos**.

Cada producto deberá tener como mínimo los siguientes 10 atributos:

```javascript
{
  id: 1,
  nombre: "Teclado mecánico RGB",
  categoria: "Periféricos",
  marca: "Logitech",
  precio: 289900,
  stock: 15,
  proveedor: "Distribuciones Tech SAS",
  fechaIngreso: "2026-07-15",
  disponible: true,
  imagen: "https://..."
}
```

Los 10 atributos obligatorios son:

1. `id`
2. `nombre`
3. `categoria`
4. `marca`
5. `precio`
6. `stock`
7. `proveedor`
8. `fechaIngreso`
9. `disponible`
10. `imagen`

Los productos deben tener información variada y coherente.

No se aceptarán 50 productos completamente idénticos en los que solamente cambie el número del identificador.

---

# Prompt sugerido para generar el JSON

Puedes utilizar el siguiente prompt en un agente de inteligencia artificial:

```text
Genera un arreglo de JavaScript con exactamente 50 productos tecnológicos.

Cada producto debe ser un objeto con los siguientes atributos:

- id
- nombre
- categoria
- marca
- precio
- stock
- proveedor
- fechaIngreso
- disponible
- imagen

Condiciones:

1. El id debe ser único y consecutivo.
2. El precio debe ser un número entero sin símbolos de moneda.
3. El stock debe ser un número entero.
4. El atributo disponible debe ser booleano.
5. La fecha debe usar el formato YYYY-MM-DD.
6. Las categorías deben incluir computadores, periféricos, celulares, accesorios, almacenamiento y componentes.
7. Los nombres, marcas, precios y proveedores deben ser variados.
8. La imagen debe contener una URL válida o una imagen de marcador de posición.
9. Entrega únicamente el arreglo de JavaScript.
10. No agregues explicaciones antes ni después del código.
```

El resultado deberá almacenarse en una constante:

```javascript
const productos = [
  // Los 50 productos
];
```

---

# Restricciones sobre el uso de inteligencia artificial

La inteligencia artificial puede utilizarse para:

* Generar el conjunto de datos.
* Consultar errores de sintaxis.
* Solicitar explicaciones sobre métodos de JavaScript.
* Obtener ideas de diseño.
* Crear imágenes o textos de prueba.

La inteligencia artificial no reemplaza la explicación del estudiante.

El estudiante deberá estar en capacidad de explicar:

* Cómo se recorre el arreglo.
* Cómo se crean los elementos HTML.
* Cómo se agrega contenido al DOM.
* Cómo funcionan los eventos implementados.
* Cómo se aplican filtros o búsquedas, en caso de utilizarlos.
* Qué partes del proyecto fueron desarrolladas o apoyadas mediante IA.

El docente podrá solicitar una explicación breve del código entregado.

---

# Funcionalidades obligatorias

## 1. Recorrido del arreglo

Los productos deberán recorrerse mediante JavaScript utilizando alguna de las siguientes alternativas:

* `for`
* `for...of`
* `forEach()`
* `map()`

No se permite escribir manualmente los 50 productos dentro del archivo HTML.

---

## 2. Creación dinámica de elementos

Los elementos utilizados para mostrar los productos deberán crearse o insertarse dinámicamente desde JavaScript.

Se pueden utilizar instrucciones como:

```javascript
document.createElement();
element.textContent;
element.classList.add();
element.appendChild();
element.append();
```

También se permite utilizar:

```javascript
innerHTML;
```

Sin embargo, se valorará especialmente el uso de métodos propios del DOM como:

* `createElement()`
* `textContent`
* `classList`
* `appendChild()`
* `append()`

---

## 3. Visualización de productos

La información podrá mostrarse utilizando una de las siguientes opciones.

### Opción A: tabla dinámica

La tabla deberá mostrar como mínimo:

* ID.
* Nombre.
* Categoría.
* Marca.
* Precio.
* Stock.
* Disponibilidad.

Ejemplo de estructura:

```html
<table>
  <thead>
    <tr>
      <th>ID</th>
      <th>Producto</th>
      <th>Categoría</th>
      <th>Marca</th>
      <th>Precio</th>
      <th>Stock</th>
      <th>Estado</th>
    </tr>
  </thead>

  <tbody id="productos-container">
    <!-- Contenido generado desde JavaScript -->
  </tbody>
</table>
```

### Opción B: tarjetas dinámicas

Cada tarjeta deberá mostrar como mínimo:

* Imagen.
* Nombre.
* Categoría.
* Marca.
* Precio.
* Stock.
* Disponibilidad.

Ejemplo del contenedor:

```html
<section id="productos-container" class="productos-grid">
  <!-- Tarjetas generadas desde JavaScript -->
</section>
```

El uso de tarjetas correctamente diseñadas otorgará puntos adicionales.

---

## 4. Formato de precios

Los precios deberán mostrarse utilizando un formato de moneda legible.

Ejemplo:

```javascript
const precioFormateado = producto.precio.toLocaleString("es-CO", {
  style: "currency",
  currency: "COP"
});
```

Resultado esperado:

```text
$289.900
```

---

## 5. Disponibilidad

El valor booleano de `disponible` no debe mostrarse solamente como `true` o `false`.

Debe transformarse en un texto comprensible para el usuario.

Ejemplo:

```javascript
const estado = producto.disponible
  ? "Disponible"
  : "No disponible";
```

Se recomienda representar visualmente el estado mediante clases CSS:

```css
.disponible {
  color: green;
}

.no-disponible {
  color: red;
}
```

---

## 6. Contador de productos

La aplicación deberá mostrar la cantidad de productos cargados.

Ejemplo:

```html
<p>
  Productos encontrados:
  <strong id="contador-productos">0</strong>
</p>
```

El valor deberá actualizarse desde JavaScript:

```javascript
contadorProductos.textContent = productos.length;
```

---

## 7. Evento obligatorio

La aplicación deberá implementar como mínimo un evento del DOM.

Puedes seleccionar una de las siguientes opciones:

* Botón para mostrar los productos.
* Botón para ocultar los productos.
* Campo para buscar productos por nombre.
* Lista para filtrar productos por categoría.
* Botón para ordenar los productos por precio.
* Botón para mostrar solamente productos disponibles.
* Botón para cambiar entre tabla y tarjetas.
* Botón para consultar los detalles de un producto.

Ejemplo:

```javascript
const botonMostrar = document.querySelector("#btn-mostrar");

botonMostrar.addEventListener("click", () => {
  mostrarProductos(productos);
});
```

---

# Recomendaciones de implementación

## Selección de elementos

Utiliza selectores del DOM para acceder a los elementos de la interfaz.

```javascript
const contenedor = document.querySelector("#productos-container");
const contador = document.querySelector("#contador-productos");
const buscador = document.querySelector("#buscador");
```

---

## Función para mostrar productos

Se recomienda separar la lógica en funciones.

```javascript
function mostrarProductos(listaProductos) {
  contenedor.textContent = "";

  listaProductos.forEach((producto) => {
    // Crear los elementos correspondientes.
    // Agregar información.
    // Insertar los elementos en el contenedor.
  });

  contador.textContent = listaProductos.length;
}
```

---

## Limpieza del contenedor

Antes de volver a mostrar productos, se debe limpiar el contenido anterior.

```javascript
contenedor.textContent = "";
```

Esto evita que los productos se dupliquen cada vez que se ejecuta una búsqueda o filtro.

---

## Carga inicial

La aplicación puede cargar los productos cuando se abra la página.

```javascript
document.addEventListener("DOMContentLoaded", () => {
  mostrarProductos(productos);
});
```

También se permite utilizar un botón para iniciar la carga.

---

# Condiciones técnicas

## HTML

El archivo HTML deberá:

* Utilizar etiquetas semánticas.
* Tener una estructura organizada.
* Conectar correctamente los archivos CSS y JavaScript.
* Tener títulos y textos relacionados con el caso empresarial.
* Contener los identificadores o clases necesarios para manipular el DOM.

Se recomienda utilizar:

```html
<header>
<nav>
<main>
<section>
<article>
<footer>
```

---

## CSS

El archivo CSS deberá:

* Estar separado del HTML.
* Utilizar clases.
* Aplicar estilos al encabezado, contenido principal y pie de página.
* Organizar adecuadamente la tabla o las tarjetas.
* Incluir estados visuales para productos disponibles y no disponibles.
* Mantener legibilidad y coherencia visual.

Se valorará:

* Uso de Flexbox.
* Uso de CSS Grid.
* Diseño adaptable.
* Estados `hover`.
* Uso coherente de colores.
* Tipografía legible.
* Espaciado consistente.
* Buena presentación de imágenes.

---

## JavaScript

El archivo JavaScript deberá:

* Estar separado del HTML.
* Seleccionar elementos del DOM.
* Recorrer el arreglo de productos.
* Crear o insertar elementos dinámicamente.
* Actualizar el contenido de la página.
* Implementar al menos un evento.
* Evitar duplicar información.
* Organizar la lógica mediante funciones.

---

# Entregables

El repositorio de GitHub deberá contener:

1. `index.html`
2. Archivo CSS.
3. Archivo JavaScript.
4. Archivo con los 50 productos.
5. Carpeta de imágenes, cuando sea necesaria.
6. Archivo `README.md`.
7. Enlace funcional de GitHub Pages.

---

# Contenido mínimo del README

El archivo `README.md` del estudiante deberá incluir:

```markdown
# TechStore

Aplicación web desarrollada como examen práctico de Front-End para demostrar el manejo del DOM y la carga dinámica de información desde JavaScript.

## Funcionalidades

- Visualización dinámica de productos.
- Carga de información desde un arreglo de objetos.
- Contador de productos.
- Formato de precios.
- Identificación de disponibilidad.
- Interacción mediante eventos del DOM.

## Tecnologías utilizadas

- HTML5
- CSS3
- JavaScript

## Autor

Nombre del estudiante:

Grupo:

## Enlace del proyecto

GitHub Pages:
```

---

# Publicación en GitHub Pages

El proyecto deberá publicarse mediante GitHub Pages.

Pasos generales:

1. Crear un repositorio público en GitHub.
2. Subir todos los archivos del proyecto.
3. Ingresar a la sección `Settings`.
4. Seleccionar `Pages`.
5. Elegir la rama principal.
6. Guardar la configuración.
7. Esperar la generación del enlace.
8. Verificar que la aplicación cargue correctamente.

El estudiante deberá entregar:

```text
URL del repositorio:

URL de GitHub Pages:
```

---

# Criterios de evaluación

| Criterio                   | Descripción                                                           | Puntaje |
| -------------------------- | --------------------------------------------------------------------- | ------: |
| Estructura HTML            | Uso correcto de HTML, etiquetas semánticas y organización general     |      10 |
| Diseño CSS                 | Presentación visual, distribución, legibilidad y coherencia           |      15 |
| Conjunto de datos          | Arreglo con 50 productos y mínimo 10 atributos                        |      10 |
| Recorrido del arreglo      | Uso correcto de ciclos o métodos de arreglos                          |      10 |
| Manipulación del DOM       | Creación, modificación e inserción dinámica de elementos              |      20 |
| Renderizado de información | Visualización correcta de los datos en tabla o estructura equivalente |      10 |
| Eventos                    | Implementación funcional de al menos un evento                        |      10 |
| Organización del código    | Uso de funciones, nombres claros y separación de responsabilidades    |       5 |
| Repositorio y README       | Organización del repositorio, documentación y GitHub Pages            |       5 |
| Funcionamiento general     | La aplicación carga y funciona sin errores críticos                   |       5 |
| **Total**                  |                                                                       | **100** |

---

# Puntos adicionales

Se podrán obtener hasta **10 puntos adicionales**.

| Mejora implementada                                                       | Puntaje adicional |
| ------------------------------------------------------------------------- | ----------------: |
| Mostrar los productos mediante tarjetas dinámicas correctamente diseñadas |                +4 |
| Implementar búsqueda por nombre                                           |                +2 |
| Implementar filtro por categoría o disponibilidad                         |                +2 |
| Implementar diseño adaptable para dispositivos móviles                    |                +2 |
| **Máximo adicional**                                                      |           **+10** |

Los puntos adicionales no reemplazan los requerimientos obligatorios.

---

# Posibles descuentos

| Situación                                          |                      Descuento |
| -------------------------------------------------- | -----------------------------: |
| No presentar exactamente 50 productos              |                      Hasta -10 |
| Tener menos de 10 atributos por producto           |                      Hasta -10 |
| Escribir los productos directamente en el HTML     |                      Hasta -20 |
| No utilizar manipulación del DOM                   |                      Hasta -30 |
| No implementar ningún evento                       |                      Hasta -10 |
| Proyecto sin estilos CSS propios                   |                      Hasta -15 |
| Enlace de GitHub Pages sin funcionamiento          |                       Hasta -5 |
| Código copiado que el estudiante no puede explicar |                  Según el caso |
| Entrega posterior al tiempo establecido            | Según indicaciones del docente |

---

# Distribución sugerida del tiempo

## Primera etapa: análisis y estructura

**Tiempo sugerido: 20 minutos**

* Leer el caso empresarial.
* Crear el repositorio.
* Organizar las carpetas.
* Definir la estructura de la interfaz.

## Segunda etapa: HTML y CSS

**Tiempo sugerido: 50 minutos**

* Construir la estructura HTML.
* Diseñar encabezado, sección principal y pie de página.
* Crear los estilos de la tabla o tarjetas.

## Tercera etapa: conjunto de datos

**Tiempo sugerido: 20 minutos**

* Utilizar un agente de inteligencia artificial.
* Generar los 50 productos.
* Revisar que tengan los 10 atributos.
* Corregir errores de sintaxis.

## Cuarta etapa: JavaScript y DOM

**Tiempo sugerido: 60 minutos**

* Seleccionar los elementos.
* Recorrer el arreglo.
* Crear los elementos.
* Agregar los productos al DOM.
* Mostrar el contador.
* Formatear precios y disponibilidad.

## Quinta etapa: eventos y mejoras

**Tiempo sugerido: 20 minutos**

* Implementar el evento obligatorio.
* Agregar búsquedas, filtros o tarjetas.

## Sexta etapa: pruebas y publicación

**Tiempo sugerido: 10 minutos**

* Revisar errores en consola.
* Validar enlaces.
* Subir cambios a GitHub.
* Comprobar GitHub Pages.

---

# Lista de verificación

Antes de entregar, verifica lo siguiente:

* [ ] El repositorio es público.
* [ ] El proyecto contiene HTML, CSS y JavaScript.
* [ ] Existen exactamente 50 productos.
* [ ] Cada producto tiene mínimo 10 atributos.
* [ ] Los productos se cargan desde JavaScript.
* [ ] Los productos no están escritos directamente en el HTML.
* [ ] Se utiliza manipulación del DOM.
* [ ] Se recorre correctamente el arreglo.
* [ ] Se muestra un contador de productos.
* [ ] Los precios tienen un formato legible.
* [ ] La disponibilidad se muestra como texto.
* [ ] Existe al menos un evento funcional.
* [ ] La tabla o las tarjetas tienen estilos CSS.
* [ ] La consola del navegador no presenta errores críticos.
* [ ] El proyecto tiene un archivo README.
* [ ] El enlace de GitHub Pages funciona.
* [ ] El nombre del estudiante aparece en el proyecto.

---

# Preguntas de sustentación

El docente podrá seleccionar algunas de las siguientes preguntas:

1. ¿Qué es el DOM?
2. ¿Cómo seleccionaste el contenedor de productos?
3. ¿Qué método utilizaste para recorrer el arreglo?
4. ¿Cuál es la diferencia entre `textContent` e `innerHTML`?
5. ¿Cómo creaste los elementos de cada producto?
6. ¿Qué función utilizaste para mostrar los productos?
7. ¿Por qué limpiaste el contenedor antes de renderizar?
8. ¿Cómo funciona el evento implementado?
9. ¿Cómo realizaste el formato de los precios?
10. ¿Cómo transformaste los valores booleanos de disponibilidad?
11. ¿Qué ocurriría si el arreglo estuviera vacío?
12. ¿Qué parte de la solución fue apoyada por inteligencia artificial?
13. ¿Qué modificarías para agregar un nuevo producto?
14. ¿Cómo implementarías un filtro por categoría?
15. ¿Cómo publicarías una nueva versión en GitHub Pages?

---

# Resultado esperado

Al abrir la aplicación, el usuario deberá encontrar una interfaz relacionada con la empresa **TechStore**.

La página deberá cargar dinámicamente los 50 productos y presentarlos de manera organizada.

La aplicación deberá mostrar:

* Información general de la empresa.
* Cantidad de productos encontrados.
* Nombre de cada producto.
* Categoría.
* Marca.
* Precio.
* Stock.
* Estado de disponibilidad.
* Imágenes o elementos visuales.
* Al menos una interacción funcional.

La interfaz deberá ser clara, navegable y visualmente coherente.

---

# Reglas finales

1. El trabajo es individual.
2. El tiempo máximo es de 3 horas.
3. El estudiante puede consultar documentación.
4. Se permite utilizar agentes de inteligencia artificial.
5. El estudiante es responsable de revisar y comprender el código generado.
6. No se permite copiar el proyecto completo de otro estudiante.
7. La información deberá cargarse dinámicamente.
8. El uso del DOM es obligatorio.
9. La entrega deberá realizarse mediante GitHub.
10. El proyecto debe funcionar desde GitHub Pages.

---

## Mensaje final

Este examen no busca evaluar únicamente que la página se vea bonita.

El propósito principal es demostrar que puedes tomar información estructurada, recorrerla, transformarla y convertirla dinámicamente en elementos visibles dentro de una aplicación web.

La inteligencia artificial puede ayudarte a generar datos o resolver dudas, pero tú debes tomar las decisiones, organizar el código y explicar cómo funciona la solución.

**Convierte los datos en una experiencia web funcional.**

