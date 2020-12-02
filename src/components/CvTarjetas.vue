<template lang="pug">
.card
    .card-image
        figure.image.is-4by3
            img.img-tarjeta(:src="tarjeta.imagen" , alt="Placeholder image")
    .card-content
        .medias
            //- .media-left
            //-     figure.image.is-48x48
            //-         img(src="https://bulma.io/images/placeholders/96x96.png" alt="Placeholder image")
            .media-content
                p.title.is-4.pb-1 {{ tarjeta.titulo }}
                p.subtitle.is-5.pb-1 {{ tarjeta.subtitulo }}
        .content
            p {{ tarjeta.descripcion }}
            //- a @bulmaio.
            a(:href="tarjeta.github", v-show="tarjeta.github") GitHub
            a.pl-1(:href="tarjeta.web", v-show="tarjeta.web") Web
            br
            p {{ tarjeta.componentes }}
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
    .card {
        box-shadow: 8px 8px 10px 0px rgba(0,0,0,0.90);
    }
    .card-content {
        background-color: #0F060B;
    }
    figure {
        background-color: #0F060B;
    }
    .img-tarjeta {
        max-width: 100% !important;
        height: auto !important;
        margin: auto !important;
    }
    .media-content p {
        color: #ECE5ED;
    }
    .content p{
        color: #CCAEE0;
    }
    .content a {
        color: #4C5AD7;
    }
</style>