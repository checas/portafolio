<template lang="pug">
nav.navbar.has-shadow.is-spaced(role="navigation" aria-label="main navigation")
    .navbar-brand
        a.navbar-item(href="#")
            img.image.is-128x128(src="../assets/svg/coding.svg")
            h1.title {{titulo}}
        a.navbar-burger.burger(:class="showMenu" role="button" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample" )
            span(aria-hidden="true")
            span(aria-hidden="true")
            span(aria-hidden="true")

    .navbar-menu#navbarBasicExample(:class="showMenu")
        .navbar-end
            a.navbar-item(:style="text_align" href="#proyectos" @click="cambiar") Proyectos
            a.navbar-item(href="#curriculum" @click="cambiar") Curriculum
            a.navbar-item(href="#footer" @click="cambiar") Contacto
</template>
<script>
export default {
    data () {
        return {
            mostrar: false
        }
    },
    computed: {
        titulo () {
            if (this.mostrar === false) {
                return 'Oculto';
            } else {
                return 'Se ve';
            }
        },
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
