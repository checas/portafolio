<template lang="pug">
.section
    //- desarrollador front end
    .columns
        .column
            h1.title.is-4 Desarrollador Front End
            h2.title.is-4 Freelance
            p 07/2020 a la actualidad
        .column
            h1.title.is-4#titulo_falso
            ul
                li Diseño UX
                li Desarrollo de componentes en Vue
                li Diseño de páginas web
    //- RT
    .tabs
            ul
    .columns
        .column
            h1.title.is-4 Representante técnico
            h2.title.is-4 Sinec S.A.
            p 03/2020 al 07/2020
        .column
            h1.title.is-4#titulo_falso
            ul
                li Planificación, gestión, supervisión y coordinación de tareas en la unidad de negocio de YPF Santa Cruz Oeste y Este
                li Ensayos de equipos de protección eléctrica de media y baja tensión
                li Realización y revisión de informes técnicos
                li Realización y revisión de planos CAO
                li Verificación y aplicación de protocolos y estándares de la empresa y cliente
    //- Ing EyM
    .tabs
            ul
    .columns
        .column
            h1.title.is-4 Ingeniero de ensayos y mediciones
            h2.title.is-4 Sinec S.A.
            p 10/2017 al 03/2020
        .column
            h1.title.is-4#titulo_falso
            ul
                li Ensayos de equipos de protección eléctrica de media y baja tensión
                li Ensayos de PAT
                li Ensayos de transformadores
                li Realización de informes técnicos
                li Realización de planos CAO
                li Diseño y porgramación de SCADA
                li Tendido y fusión de fibra optica
    //- Prog freelance
    .tabs
            ul
    .columns
        .column
            h1.title.is-4 Programador web y mobile
            h2.title.is-4 Freelance
            p 03/2017 al 10/2017
        .column
            h1.title.is-4#titulo_falso
            ul
                li Diseño de páginas web
                li Desarrollo de aplicaciones Android
                li Desarrollo de una web app para facturación de servicio de agua potable
                    ol
                        li Dieño de interfaz en Angular y Boostrap
                        li Manejo de base de datos MySQL
                        li Diseño y desarrollo de apliación Android para relevamiento de medidores
    //- Técnico en iFix
    .tabs
            ul
    .columns
        .column
            h1.title.is-4 Técnico en reparación celulares
            h2.title.is-4 iFix
            p 02/2017 al 03/2017
        .column
            h1.title.is-4#titulo_falso
            ul
                li Reparación de teléfonos celulares
                li Reparación de tablets
    //- Perito tecnico
    .tabs
            ul
    .columns
        .column
            h1.title.is-4 Perito técnico (pasante)
            h2.title.is-4 EPRE
            p 08/2015 al 11/2016
        .column
            h1.title.is-4#titulo_falso
            ul
                li Generación y cierre de expedientes
                li Relevamiento de obras en la vía pública
                li Generación de notas ante anomalías o infracciones en la red de distribución en la vía pública
</template>
<style scoped>
li {
    list-style-type: circle;
}
h1, h2 {
    color:#ECE5ED;
}
li, p {
    color: #CCAEE0;
}
.tabs, ul {
    border-bottom-color: #B30189;
}
@media screen and (max-width: 767px) {
    .section {
        padding-top: 15px;
        padding-bottom: 15px;
    }
    #titulo_falso {
        margin-bottom: 0 !important;
    } 
}
@media screen and (max-width: 480px) {
    .section {
        padding-top: 10px;
        padding-bottom: 10px;
    }
    h1.title.is-4, h2.title.is-4 {
        margin-bottom: 5px;
    }
}
</style>