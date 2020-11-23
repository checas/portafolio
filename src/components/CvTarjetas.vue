<template lang="pug">
.card
    .card-image
        figure.image.is-4by3
            img(:src="tarjeta.imagen" , alt="Placeholder image")
    .card-content
        .media
            //- .media-left
            //-     figure.image.is-48x48
            //-         img(src="https://bulma.io/images/placeholders/96x96.png" alt="Placeholder image")
            .media-content
                p.title.is-4.has-text-white-bis {{ tarjeta.titulo }}
                p.subtitle.is-6.has-text-white-ter {{ tarjeta.subtitulo }}
        .content
            p.has-text-grey-light {{ tarjeta.descripcion }}
            //- a @bulmaio.
            a(href="#") GitHub
            a.pl-1(:href="tarjeta.web") Web
            br
            p.has-text-grey-light {{ tarjeta.componentes }}
</template>
<script>
export default {
    name:'CvTarjeta',
    data () {
        return {
            imagen: '../assets/banner.png'
        }
    },
    props: {
        tarjeta: Object
    }
}
</script>
<style scoped>
    .card-content{
        background-color: #242424;
    }
</style>