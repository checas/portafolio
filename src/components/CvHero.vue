<template lang="pug">
section.hero.is-medium.is-spaced.is-bold.tiene-fondo
    .blured-background
    .hero-body
        .columns
            .column.ml-6.is-one-third
                figure.image.foto-perfil
                    img.is-rounded(src="../assets/foto.jpg" alt="mi foto")
            .column.mr-6
                .container
                    h1.title.has-text-white Sergio Checcarelli
                    h1.has-text-white.title.is-4 Ingeniero Electrónico
                    p.has-text-white.title.is-6 Tras años de experiencia, he tomado la decisión de reorientar mi carrera profesional con el ánimo de continuar aprendiendo y, también, aportar toda mi experiencia adquirida.
                    p.has-text-white.title.is-6 Considero que el cambio es un signo de capacidad de superación.
                    p.has-text-white.title.is-6 Soy una persona emprendedora, que trabaja en equipo, adora los retos y no se rinde fácilmente. Detallista y autodidacta, nunca dejo de aprender.
</template>
<style scoped>
.foto-perfil {
    width: 250px;
    height: 250px;
}
.tiene-fondo {
        background-image: url('/img/fondo-hero-blur.jpg');
        background-position: center center;
        background-repeat:  no-repeat;
        background-attachment: fixed;
        background-size:  cover;
        background-color: #999;
}
@media screen and (max-width: 767px) {
    .column.ml-6.is-one-third{
        display: flex;
        justify-content: center;
        margin-left: 0 !important;
    }
    .column {
        text-align: center;
        padding-left: 0px;
        padding-right: 0px;
        margin-right: 0 !important;
    }
    p {
        -webkit-text-stroke: 0.4px black;
    }
}
@media screen and (max-width: 480px) {
    .column.ml-6.is-one-third{
        display: flex;
        justify-content: center;
        margin-left: 0 !important;
    }
    .column {
        text-align: center;
        padding-left: 0px;
        padding-right: 0px;
        margin-right: 0 !important;
    }
    p {
        -webkit-text-stroke: 0.4px black;
    }
}
</style>