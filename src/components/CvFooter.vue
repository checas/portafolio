<template lang="pug">
footer.footer
    .columns
        .column
            p.is-flex.is-align-content-center
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512">
                    <path d="M467 61H45C20 61 0 81 0 106v300c0 25 20 45 45 45h422c25 0 45-20 45-45V106c0-25-20-45-45-45zm-6 30L257 295 51 91h410zM30 400V112l144 143L30 400zm21 21l145-145 50 51c6 5 16 5 22 0l49-50 144 144H51zm431-21L338 256l144-144v288z"/>
                </svg>
                strong.pl-2 checcarelli.s@gmail.com
        .column
            p.is-flex.is-align-content-center.is-flex-direction-row
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 387.2 387.2">
                    <path d="M305 11c-7-7-16-11-26-11H108C88 0 72 16 72 37v313a37 37 0 0036 37h171a37 37 0 0037-37V37c0-10-4-19-11-26zM194 362a10 10 0 110-20 10 10 0 010 20zm92-62c0 13-10 24-24 24H125c-14 0-24-11-24-24V66c0-13 10-24 24-24h137c14 0 24 11 24 24v234z"/>
                </svg>
                strong.pl-2 +54-294-4898392
        .column
            a.is-flex.is-align-content-center(href="https://github.com/checas")
                <svg height="512" viewBox="0 0 24 24" width="512" xmlns="http://www.w3.org/2000/svg">
                    <path d="M12 1C5 1 0 6 0 12s3 10 8 11h1v-2c-3 1-4-2-4-2l-1-1v-1l2 1c1 2 2 1 3 1l1-1c-3-1-6-2-6-6 0-2 1-3 2-3V5l3 2a12 12 0 016 0l3-2v4c1 0 2 1 2 3 0 4-3 5-6 5l1 3v3h1c5-1 8-6 8-11 0-6-5-12-12-12z"/>
                </svg>
                strong.pl-2 github/checas.com
        .column
            a.is-flex.is-align-content-center(href="https://www.linkedin.com/in/sergio-checcarelli/")
                <svg height="512" viewBox="0 0 24 24" width="512" xmlns="http://www.w3.org/2000/svg">
                    <path d="M24 24v-9c0-4-1-7-6-7l-5 2V8H8v16h5v-8c0-2 1-4 3-4 3 0 3 2 3 4v8zM0 8h5v16H0zM3 0C1 0 0 1 0 3s1 3 3 3 3-2 3-3c0-2-2-3-3-3z"/>
                </svg>
                strong.pl-2 sergio-checcarelli
        .column
            a.is-flex.is-align-content-center(href="https://www.instagram.com/checa_s/")
                <svg viewBox="0 0 512 512" xmlns="http://www.w3.org/2000/svg">
                    <path d="M373 0H139C62 0 0 62 0 139v234c0 77 62 139 139 139h234c77 0 139-62 139-139V139C512 62 450 0 373 0zm109 373c0 60-49 109-109 109H139c-60 0-109-49-109-109V139C30 79 79 30 139 30h234c60 0 109 49 109 109zm0 0"/><path d="M256 116a140 140 0 100 280 140 140 0 000-280zm0 250a110 110 0 110-220 110 110 0 010 220zm0 0M399 66a41 41 0 100 83 41 41 0 000-83zm0 53a11 11 0 110-23 11 11 0 010 23zm0 0"/>
                </svg>
                strong.pl-2 checa_s
    br
    h1.title.has-text-centered.is-5 💻 by Sergio Checcarelli
</template>
<style scoped>
footer{
    background-color: #2D1062;
}
a, strong, h1{
    color: #ECE5ED;
}
svg {
    height: 24px;
    width: auto;
    fill: #ECE5ED;
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