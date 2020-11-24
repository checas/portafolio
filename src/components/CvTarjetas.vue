<template lang="pug">
.card
    .card-image
        figure.image.is-4by3.has-background-black-bis
            img.img-tarjeta(:src="tarjeta.imagen" , alt="Placeholder image")
    .card-content
        .medias
            //- .media-left
            //-     figure.image.is-48x48
            //-         img(src="https://bulma.io/images/placeholders/96x96.png" alt="Placeholder image")
            .media-content
                p.title.is-4.has-text-white-bis.pb-1 {{ tarjeta.titulo }}
                p.subtitle.is-5.has-text-white-ter.pb-1 {{ tarjeta.subtitulo }}
        .content
            p.p.has-text-white-ter {{ tarjeta.descripcion }}
            //- a @bulmaio.
            a(:href="tarjeta.github", v-show="tarjeta.github") GitHub
            a.pl-1(:href="tarjeta.web", v-show="tarjeta.web") Web
            br
            p.p.has-text-white-ter {{ tarjeta.componentes }}
</template>
<script>
export default {
    name:'CvTarjeta',
    props: {
        tarjeta: Object
    }
}
</script>
<style scoped>
    .card-content{
        background-color: #242424;
    }
    .img-tarjeta {
        max-width: 100% !important;
        height: auto !important;
        margin: auto !important;
    }
</style>