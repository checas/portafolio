<template lang="pug">
.section
    .columns
        .column
            h1.title.is-4 Desarrollador Front End
            h2.title.is-4 Platzi
            p 03/2020 a la actualidad
        .column
            h1.title.is-4 Fotografía Digital
            h2.title.is-4 Platzi
            p 05/2020 al 07/2020
    .columns
        .column
            h1.title.is-4 SCADA, IFix fundamentals
            h2.title.is-4 GE
            p 06/2020
        .column
            h1.title.is-4 Desarrollador Front End
            h2.title.is-4 Acamica
            p 12/2016 al 07/2017
    .columns
        .column
            h1.title.is-4 Desarrollador Back End
            h2.title.is-4 Acamica
            p 12/2016 al 07/2017
        .column
            h1.title.is-4 Desarrollador web
            h2.title.is-4 Acamica
            p 12/2016 al 07/2017
    .columns
        .column
            h1.title.is-4 Diseñador web
            h2.title.is-4 Acamica
            p 12/2016 al 04/2017
</template>
<style scoped>
h1, h2 {
    color:#ECE5ED;
}
p {
    color: #CCAEE0;
}
@media screen and (max-width: 767px) {
    .section {
        padding-top: 15px;
        padding-bottom: 15px;
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