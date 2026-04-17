## 𐙚 ‧₊˚ ⋅ Pagina Web sobre La Cienega de Mallorquín

૮ ˶ᵔ ᵕ ᵔ˶ ა  
#### Esta es una pagina web, que utiliza algunos metodos de **flexbox**, **CSS Grid**, *margin*, *padding* y en general todo lo referenta a modelo de caja de css. Se intenta llevar una buena semantica en el html con el objetivo de emular una buena interfaz de usuario, agradable y landeable.
---

## 𐙚 ‧₊˚ ⋅ Project Overview

Este proyecto tiene las funciones o vistas principales

- Permite llegar a links por medio de un **navbar**
- Se puede ver un **mapa de google maps en tiempo real**
- Tiene las normas básicas de cuidado **en espacios ecologicos**
- Su interfaz es atractiva porqué **tiene animaciones**

---

## 𐙚 ‧₊˚ ⋅ Program Structure

### 📚 Meta etiquets
```html
<head>
    <meta charset="UTF-8">
    <meta name="Cienega de mallorquin" content="Una pagina no oficial de la cienega de mallorquin">
    <link rel="stylesheet" href="assets/css/style.css">
    <meta name="keywords" content="Ciénega, ecología, ecoparque, senderismo, turismo sostenible">
    <title>Ciénega de mallorquín_ página no oficial ❁</title>
</head>
```
El programa necesita estas etiquetas para el seo (search engine optimization), estas etiquetas funcionan para que el navegador web asocie las etiquetas, las keywords y el titule con el contenido de nuestro sitio web. La razón por la cual se utiliza las siguientes keywords:

```html
<meta name="keywords" content="Ciénega, ecología, ecoparque, senderismo, turismo sostenible">
```
Es para que el navegador asocie las keywords con cada resultado de busqueda sobre esas palabras, es decir, sí se busca alguna de estas palabras puede aparecer facilmente.
---

### 📚¿Porque se manejan tantos divs y sections?

#### En este proyecto se decidió manejar sections y div, para que el css sea manejable y poder hacer cuadros de textos atractivos a la vista. ¿Como se logro esto?, sencillo, se llamaba una clase al div, luego se colocanban los respectivos objetos, por ultimo se editaban en el css y se les colocaban las caracteristicas como el blureado, o las animaciones directamente a la clase.
### Ejemplo:
```html
<nav class="navbar">  /*Aca se guarda en una clase*/
        <span>Eco parque <br> Mallorquín</span> /*este es un objeto*/
        <a href="https://ecoturismocienagademallorquin.com/" target="_blank">Información oficial</a>  /*este es otro objeto*/
        <a href="https://ecoturismocienagademallorquin.com/fiesta-de-la-virgen-del-carmen-de-los-pescadores/" target="_blank"> Conoce sus costumbres</a>
        <a href="https://agendacolombia.com/barranquilla/guia-del-ecoparque-mallorquin-en-barranquilla/" target="_blank">Eventos</a>
        <a href="https://www.elespectador.com/ambiente/blog-el-rio/la-disputa-por-las-obras-alrededor-de-la-cienaga-mas-importante-de-barranquilla/" target="_blank">Noticias</a>
    </nav>
```
- luego se revisa el css y mira que se opera para que el resultado sea agradable a la vista

```css
.navbar {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    height: 9rem;
    background-color: #1A5126;
    color:aliceblue;
}

.navbar span {
    
    font-size: 3rem;
}

.navbar a {
    color: #8fbf5f;
    text-decoration: none;
}

.navbar a:hover {
    color: #218618;
}

```

---

