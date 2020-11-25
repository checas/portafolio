<template lang="pug">
nav.navbar.has-shadow.is-spaced(role="navigation" aria-label="main navigation")
    .navbar-brand
        a.navbar-item(href="#")
            img.image.is-128x128(src="../assets/svg/coding.svg")
            h1.title Sergio Checcarelli
        a.navbar-burger.burger.mr-5(:class="showMenu" role="button" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample" @click="cambiar")
            span(aria-hidden="true")
            span(aria-hidden="true")
            span(aria-hidden="true")

    .navbar-menu(:class="showMenu")
        .navbar-end
            a.navbar-item(:style="text_align" @click="cambiar" href="#proyectos") Proyectos
            a.navbar-item(:style="text_align" @click="cambiar" href="#curriculum") Curriculum
            a.navbar-item(:style="text_align" @click="cambiar" href="#footer") Contacto
</template>

<style scoped>
.navbar-link:not(.is-arrowless)::after {
    border-color: red;
}
a.navbar-item:focus, a.navbar-item:focus-within, a.navbar-item:hover, a.navbar-item.is-active, .navbar-link:focus, .navbar-link:focus-within, .navbar-link:hover, .navbar-link.is-active {
    color: red
}
@media screen and (max-width: 767px) {
    
}
@media screen and (max-width: 480px) {
    img.image.is-128x128 {
        max-height: 1.5rem;
    }
    h1.title {
        font-size: 1.5rem;
    }
}
@media screen and (max-width: 480px) {
    img.image.is-128x128 {
        max-height: 1.2rem;
    }
    h1.title {
        font-size: 1.3rem;
    }
}
@media screen and (max-width: 320px) {
    img.image.is-128x128 {
        max-height: 1rem;
        width: auto;
        padding-right: 15px;
    }
    h1.title {
        font-size: 1.3rem;
    }
    a.navbar-burger.burger.mr-5 {
        margin-right: 5px !important;
    }
}

</style>
<script>
export default {
    data () {
        return {
            mostrar: false
        }
    },
    computed: {
        showMenu () {
            if (this.mostrar === true) {
                return 'is-active'
            } else {
                return ''
            }
        },
        text_align () {
            if (this.mostrar === true) {
                return 'text-align: center'
            } else {
                return ''
            }
        }
    },
    methods: {
        cambiar () {
            this.mostrar = !this.mostrar;
        }
    }
}
</script>