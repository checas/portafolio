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
            .navbar-item.has-dropdown.is-hoverable
                a.navbar-link Proyectos
                .navbar-dropdown
                    a.navbar-item Trabajos freelance
                    hr.navbar-divider
                    a.navbar-item Propios
                    hr.navbar-divider
                    a.navbar-item De cursos
            a.navbar-item Curriculum
            a.navbar-item Contacto
</template>

<style scoped>
.navbar-link:not(.is-arrowless)::after {
    border-color: red;
}
a.navbar-item:focus, a.navbar-item:focus-within, a.navbar-item:hover, a.navbar-item.is-active, .navbar-link:focus, .navbar-link:focus-within, .navbar-link:hover, .navbar-link.is-active {
    color: red
}    
</style>