<template lang="pug">
div    
    .columns
        .column
            cv-tarjetas(:tarjeta="proyectos[0]", v-show="showPagina1")
            cv-tarjetas(:tarjeta="proyectos[3]", v-show="!showPagina1")
        .column
            cv-tarjetas(:tarjeta="proyectos[1]", v-show="showPagina1")
        .column
            cv-tarjetas(:tarjeta="proyectos[2]", v-show="showPagina1")
    nav.pagination.is-right(role="navigation" aria-label="pagination")
        a.pagination-previous(:disabled="showAnterior", @click="cambiarPagina1") Anterior
        a.pagination-next(:disabled="showSiguiente", @click="cambiarPagina2") Siguiente
        ul.pagination-list
            li
                a.pagination-link(aria-label="Goto page 1", :disabled="showPagina1", @click="cambiarPagina1") 1
            //- li
            //-     span.pagination-ellipsis &hellip;
            li
                a.pagination-link.disable(aria-label="Goto page 2", :disabled="showPagina2", @click="cambiarPagina2") 2
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
    name: 'Proyectos_Freelance',
    components: {
        CvTarjetas
    },
    data () {
        return {
            showPagina1: true,
            showPagina2: false,
            showSiguiente: false,
            showAnterior: true,
            proyectos: [
                {
                    titulo: 'Web-app para facturación',
                    subtitulo: 'Desarrollo de una web-app',
                    descripcion: 'Esta es una versión actualizada de un proyecto anterior. Se tomó como base el sistema de facturación para agua potable, pero se actualizaron las tecnologías con las que se desarrolló',
                    componentes: '#Laravel, #Vue, #MySQL',
                    github: 'https://github.com/diegocheca/laravue',
                    imagen: '/img/sistema_nuevo.png'
                },
                {
                    titulo: 'Página web publicitaria',
                    subtitulo: 'Diseño de un página web para la presentación del sistema de facturación',
                    descripcion: 'Desarrollo de un página web estatica para la promoción del sistema de facturación',
                    componentes: '#HTML, #CSS, #Boostrap, #JavaScript',
                    github: 'https://github.com/checas/AquaPage',
                    web: 'https://checas.github.io/AquaPage/',
                    imagen: '/img/pagina_agua.png'
                },
                {
                    titulo: 'Aplicación para relevamiento de medidores',
                    subtitulo: 'Desarrollo de una app para android',
                    descripcion: 'La aplicación permite realizar el relevamiento de los medidores de agua potable de cada usuario con servicio. Esta app se conecta mediante wifi para actualizar la base de datos del sistema, como así también, recibir a principio de mes la nueva base de datos para realizar las mediciones',
                    componentes: '#Android, #Java',
                    imagen: '/img/app_villaEliza.png',
                    github: 'https://github.com/checas/VillaElisa_Mediciones',
                },
                {
                    titulo: 'Web app para facturación de servicio de agua potable',
                    subtitulo: 'Desarrollo de un sistema de facturación',
                    descripcion: 'Sistema para facturación, manejo de clientes, manejo de materiales, manejo de ordenes de trabajo, generación de facturas, envío de mails y generación de informes',
                    componentes: '#PHP, #Codeigniter, #Angular, #Boostrap, #MySQL',
                    imagen: '/img/sistema_viejo.jpg'
                },
            ],

        }
    },
    methods: {
        cambiarPagina1 () {
            this.showPagina1 = true;
            this.showPagina2 = false;
            this.showAnterior = true;
            this.showSiguiente = false;
        },
        cambiarPagina2 () {
            this.showPagina1 = false;
            this.showPagina2 = true;
            this.showAnterior = false;
            this.showSiguiente = true;
        }
    },
}
</script>
