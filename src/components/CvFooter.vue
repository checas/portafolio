<template lang="pug">
footer.footer
    .columns
        .column
            p.is-flex.is-align-content-center
                img.image.is-24x24(src="../assets/svg/001-email.svg")
                strong.pl-2 checcarelli.s@gmail.com
        .column
            p.is-flex.is-align-content-center.is-flex-direction-row
                img.image.is-24x24(src="../assets/svg/004-phone.svg")
                strong.pl-2 +54-294-4898392
        .column
            a.is-flex.is-align-content-center(href="https://github.com/checas")
                img.image.is-24x24(src="../assets/svg/002-github.svg")
                strong.pl-2 github/checas.com
        .column
            a.is-flex.is-align-content-center(href="https://www.linkedin.com/in/sergio-checcarelli/")
                img.image.is-24x24(src="../assets/svg/007-linkedin.svg")
                strong.pl-2 sergio-checcarelli
        .column
            a.is-flex.is-align-content-center(href="https://www.instagram.com/checa_s/")
                img.image.is-24x24(src="../assets/svg/006-instagram-1.svg")
                strong.pl-2 checa_s
    br
    h1.title.has-text-centered.is-5 💻 by Sergio Checcarelli
</template>
<style scoped>
a {
    color: #363636;
}
@media screen and (max-width: 767px) {
    footer {
        padding-top: 20px;
        padding-bottom: 20px;
    }
    .columns {
        margin-top: 5px;
        margin-bottom: 5px;
    }
    .column {
        display: flex;
        justify-content: center;
    }
}
@media screen and (max-width: 480px) {
    footer {
        padding-top: 15px;
        padding-bottom: 15px;
    }
}
</style>