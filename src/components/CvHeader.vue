<template lang="pug">
nav.navbar.has-shadow.is-spaced(role="navigation" aria-label="main navigation")
    .navbar-brand
        a.navbar-item(href="#")
            img.image.is-128x128(src="../assets/svg/coding.svg")
            h1.title Sergio Checcarelli
        a.navbar-burger.burger(role="button" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample")
            span(aria-hidden="true")
            span(aria-hidden="true")
            span(aria-hidden="true")

    .navbar-menu#navbarBasicExample
        .navbar-end
            a.navbar-item(href="#proyectos") Proyectos
            a.navbar-item(href="#curriculum") Curriculum
            a.navbar-item(href="#footer") Contacto
</template>

<style scoped>
.navbar-link:not(.is-arrowless)::after {
    border-color: red;
}
a.navbar-item:focus, a.navbar-item:focus-within, a.navbar-item:hover, a.navbar-item.is-active, .navbar-link:focus, .navbar-link:focus-within, .navbar-link:hover, .navbar-link.is-active {
    color: red
}    
</style>