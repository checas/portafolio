<template lang="pug">
div
    h1 De cursos
</template><template lang="pug">
div    
    .columns
        .column
            cv-tarjetas(:tarjeta="proyectos[0]", v-show="showPagina1")
            cv-tarjetas(:tarjeta="proyectos[3]", v-show="showPagina2")
            cv-tarjetas(:tarjeta="proyectos[6]", v-show="showPagina3")
            cv-tarjetas(:tarjeta="proyectos[9]", v-show="showPagina4")
        .column
            cv-tarjetas(:tarjeta="proyectos[1]", v-show="showPagina1")
            cv-tarjetas(:tarjeta="proyectos[4]", v-show="showPagina2")
            cv-tarjetas(:tarjeta="proyectos[7]", v-show="showPagina3")
            cv-tarjetas(:tarjeta="proyectos[10]", v-show="showPagina4")
        .column
            cv-tarjetas(:tarjeta="proyectos[2]", v-show="showPagina1")
            cv-tarjetas(:tarjeta="proyectos[5]", v-show="showPagina2")
            cv-tarjetas(:tarjeta="proyectos[8]", v-show="showPagina3")
    nav.pagination.is-right(role="navigation" aria-label="pagination")
        a.pagination-previous(:disabled="showAnterior", @click="cambiarAnterior") Anterior
        a.pagination-next(:disabled="showSiguiente", @click="cambiarSiguiente") Siguiente
        ul.pagination-list
            li
                a.pagination-link(aria-label="Goto page 1", :disabled="show1", @click="cambiarPagina1") 1
            //- li
            //-     span.pagination-ellipsis &hellip;
            li
                a.pagination-link.disable(aria-label="Goto page 2", :disabled="show2", @click="cambiarPagina2") 2
            li
                a.pagination-link.disable(aria-label="Goto page 3", :disabled="show3", @click="cambiarPagina3") 3
            li
                a.pagination-link.disable(aria-label="Goto page 4", :disabled="show4", @click="cambiarPagina4") 4
            //- li
            //-     a.pagination-link.is-current(aria-label="Page 46" aria-current="page") 46
            //- li
            //-     a.pagination-link(aria-label="Goto page 47") 47
            //- li
            //-     span.pagination-ellipsis &hellip;
            //- li
            //-     a.pagination-link(aria-label="Goto page 86") 86
</template>
<style scoped>
    a {
        color: #2D1062;
        background-color: #ECE5ED;
        border-color: #4C5AD7;
        border-radius: 25px;
    }
</style>
<script>
import CvTarjetas from '../components/CvTarjetas.vue'
export default {
    name: 'Proyectos_Cursos',
    components: {
        CvTarjetas
    },
    data () {
        return {
            showPagina1: true,
            showPagina2: false,
            showPagina3: false,
            showPagina4: false,
            show1: true,
            show2: false,
            show3: false,
            show4: false,
            showSiguiente: false,
            showAnterior: true,
            proyectos: [
                {
                    titulo: 'Diseño de página para convención',
                    subtitulo: 'Diseño utilizando boostrap',
                    descripcion: 'Página para presentación de una convención',
                    componentes: '#HTML, #Boostrap',
                    github: 'https://github.com/checas/Curso-Boostrap',
                    web: 'https://checas.github.io/Curso-Boostrap/',
                    imagen: '/img/boostrap.png'
                },
                {
                    titulo: 'Diseño de banner',
                    subtitulo: 'Diseño utilizando css grid',
                    descripcion: 'Uso de CSS grid para realizar el diseño',
                    componentes: '#HTML, #CSS',
                    github: 'https://github.com/checas/ejercicio-css-grid',
                    web: 'https://checas.github.io/ejercicio-css-grid/',
                    imagen: '/img/banner.png'
                },
                {
                    titulo: 'Maquetación en HTML y CSS',
                    subtitulo: 'Diseño de página de inició de Google',
                    descripcion: 'Maquetación de página web utilizando HTML y CSS',
                    componentes: '#HTML, #CSS',
                    github: 'https://github.com/checas/curso-practico-html-y-css',
                    web: 'https://checas.github.io/curso-practico-html-y-css/',
                    imagen: '/img/html_css_practico.png'
                },
                {
                    titulo: 'Diseño de página web de videos',
                    subtitulo: 'Uso de JQuerry',
                    descripcion: 'Uso de JQuerry para el manejo de una api de peliculas y CSS grid para el diseño',
                    componentes: '#HTML, #CSS, #JQuerry',
                    github: 'https://github.com/checas/cursos-jquerry',
                    web: 'https://checas.github.io/cursos-jquerry/',
                    imagen: '/img/pagina_videos.png'
                },
                {
                    titulo: 'Juego de memoria',
                    subtitulo: 'Uso de JS',
                    descripcion: 'Uso de JS para generar las secuencias y obtener las respuestas por parte del usuario',
                    componentes: '#HTML, #CSS, #JavaScript',
                    github: 'https://github.com/checas/ejercicio-js-basico',
                    web: 'https://checas.github.io/ejercicio-js-basico/',
                    imagen: '/img/juego_memoria.png'
                },
                {
                    titulo: 'Maquetado web',
                    subtitulo: 'Diseño de un blog',
                    descripcion: 'Uso de HTML y CSS para el diseño de un blog',
                    componentes: '#HTML, #CSS',
                    github: 'https://github.com/checas/ejercicio-maquetado',
                    web: 'https://checas.github.io/ejercicio-maquetado/',
                    imagen: '/img/maquetado_blog.png',
                },
                {
                    titulo: 'Diseño de página sobre viedo juegos',
                    subtitulo: 'Uso de preprocesadores',
                    descripcion: 'Uso de PUG y SASS para realizar el diseño',
                    componentes: '#PUG, #SASS',
                    github: 'https://github.com/checas/ejercicio-preprocesadores',
                    web: 'https://checas.github.io/ejercicio-preprocesadores/',
                    imagen: '/img/blog_juegos.png'
                },
                {
                    titulo: 'Maquetación web',
                    subtitulo: 'Diseño de un portafolio ',
                    descripcion: 'Uso de HTML y CSS para realizar una página responsive',
                    componentes: '#HTML, #CSS',
                    github: 'https://github.com/checas/ejercicio-responsive-design',
                    web: 'https://checas.github.io/ejercicio-responsive-design/',
                    imagen: '/img/maquetado_portafolio.png'
                },
                {
                    titulo: 'Single page aplication',
                    subtitulo: 'JavaScript',
                    descripcion: 'Uso de JavaScript para realizar una single page aplication y uso de API',
                    componentes: '#HTML, #CSS',
                    github: 'https://github.com/checas/ejercicio-single-page-js',
                    web: 'https://checas.github.io/ejercicio-single-page-js/',
                    imagen: '/img/single_page_js.png'
                },
                {
                    titulo: 'Single page aplication',
                    subtitulo: 'Web para visualizar precios de cripto monedas',
                    descripcion: 'Uso de Vue.js para generar una single page, generación de modulos, uso de api, vue route y tailwind',
                    componentes: '#HTML, #Vue.js, #Tailwind',
                    github: 'https://github.com/checas/platziExchange',
                    web: 'https://platziechange.netlify.app/',
                    imagen: '/img/vue_crypto.png'
                },
                {
                    titulo: 'Single page aplication',
                    subtitulo: 'Web para buscar y reproducir música',
                    descripcion: 'Uso de Vue.js para generar una single page, utilizando una variante de la api de Spotify para buscar y reporducir música. Uso de vue router y i18n',
                    componentes: '#PUG, #Bulma, #Vue.js',
                    github: 'https://github.com/checas/platzi-music',
                    web: 'https://platzi-music.netlify.app/',
                    imagen: '/img/vue_music.png'
                },
            ],
        }
    },
    methods: {
        cambiarSiguiente () {
            if(this.showPagina1 === true){
                this.cambiarPagina2();
            } else if(this.showPagina2 === true){
                this.cambiarPagina3();
            } else if(this.showPagina3 === true){
                this.cambiarPagina4();
            } else if(this.showPagina4 === true){
                this.cambiarPagina4();
            } 
        },
        cambiarAnterior () {
            if(this.showPagina1 === true) {
                this.cambiarPagina1();
            } else if(this.showPagina2 === true) {
                this.cambiarPagina1(); 
            } else if(this.showPagina3 === true) {
                this.cambiarPagina2(); 
            } else if(this.showPagina4 === true) {
                this.cambiarPagina3();
            }
        },
        cambiarPagina1 () {
            this.showPagina1 = true;
            this.showPagina2 = false;
            this.showPagina3 = false;
            this.showPagina4 = false;
            this.show1 = true;
            this.show2 = false;
            this.show3 = false;
            this.show4 = false;
            this.showAnterior = true;
            this.showSiguiente = false;
        },
        cambiarPagina2 () {
            this.showPagina1 = false;
            this.showPagina2 = true;
            this.showPagina3 = false;
            this.showPagina4 = false;
            this.show1 = false;
            this.show2 = true;
            this.show3 = false;
            this.show4 = false;
            this.showAnterior = false;
            this.showSiguiente = false;
        },
        cambiarPagina3 () {
            this.showPagina1 = false;
            this.showPagina2 = false;
            this.showPagina3 = true;
            this.showPagina4 = false;
            this.show1 = false;
            this.show2 = false;
            this.show3 = true;
            this.show4 = false;
            this.showAnterior = false;
            this.showSiguiente = false;
        },
        cambiarPagina4 () {
            this.showPagina1 = false;
            this.showPagina2 = false;
            this.showPagina3 = false;
            this.showPagina4 = true;
            this.show1 = false;
            this.show2 = false;
            this.show3 = false;
            this.show4 = true;
            this.showAnterior = false;
            this.showSiguiente = true;
        }
    },
    cambiarPaginaAnterior (){
        console.log('pagina anterior');
    },
    cambiarPaginaSiguiente (){
        console.log('pagina siguiente');
    }
}
</script>