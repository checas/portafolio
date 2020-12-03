<template lang="pug">
.section
    .container
        h1.title Curriculum
        .tabs
            ul
                li(:class="antecedentesClass")
                    a.title.is-5(@click="antecedentesSelect") Antecedentes laborales
                li(:class="habilidadesClass")
                    a.title.is-5(@click="habilidadesSelect") Habilidades
                li(:class="estudiosClass")
                    a.title.is-5(@click="estudiosSelect") Estudios
                li(:class="cursosClass")
                    a.title.is-5(@click="cursosSelect") Cursos
        transition(name="fade")
            div(v-show="showAntecedentes")
                cv-antecedentes
        transition(name="fade")
            div(v-show="showHabilidades")
                cv-habilidades
        transition(name="fade")
            div(v-show="showEstudios")
                cv-estudios
        transition(name="fade")
            div(v-show="showCursos")
                cv-cursos
</template>
<script>

import CvAntecedentes from './CvAntecedentes.vue'
import CvHabilidades from './CvHabilidades.vue'
import CvEstudios from './CvEstudios.vue'
import CvCursos from './CvCursos.vue'

export default {
    components:{ CvAntecedentes, CvHabilidades, CvEstudios, CvCursos },
    data () {
        return {
            antecedentesClass: 'is-active',
            habilidadesClass: '',
            estudiosClass: '',
            cursosClass: '',
            showAntecedentes: true,
            showHabilidades: false,
            showEstudios: false,
            showCursos: false
        }
    },
    methods: {
        antecedentesSelect(){
            this.antecedentesClass = 'is-active';
            this.habilidadesClass = '';
            this.estudiosClass = '';
            this.cursosClass = '';
            this.showAntecedentes = true;
            this.showHabilidades = false;
            this.showEstudios = false;
            this.showCursos = false;
        },
        habilidadesSelect(){
            this.antecedentesClass = '';
            this.habilidadesClass = 'is-active';
            this.estudiosClass = '';
            this.cursosClass = '';
            this.showAntecedentes = false;
            this.showHabilidades = true;
            this.showEstudios = false;
            this.showCursos = false;
        },
        estudiosSelect(){
            this.antecedentesClass = '';
            this.habilidadesClass = '';
            this.estudiosClass = 'is-active';
            this.cursosClass = '';
            this.showAntecedentes = false;
            this.showHabilidades = false;
            this.showEstudios = true;
            this.showCursos = false;
        },
        cursosSelect(){
            this.antecedentesClass = '';
            this.habilidadesClass = '';
            this.estudiosClass = '';
            this.cursosClass = 'is-active';
            this.showAntecedentes = false;
            this.showHabilidades = false;
            this.showEstudios = false;
            this.showCursos = true;
        }
    }
}
</script>
<style scoped>
h1 {
    color: #ECE5ED;
}
li a {
    color: #CCAEE0;
}
.tabs ul {
    border-color: #B30189;
}
.tabs a {
    border-color: #B30189;
}
.tabs li a:hover{
    color:#B30189;
}
li, a {
    border-color: #B30189;
}
.section {
    background-color: #0F060B;
}
.tabs li.is-active a {
    border-color: #ECE5ED;
    color: #ECE5ED !important;
}
.fade-enter-active, .fade-leave-active {
    transition: opacity .2s
}
.fade-enter, .fade-leave-to {
    opacity: 0
}
@media screen and (max-width: 767px) {
    h1.title.has-text-white-bis {
        text-align: center;
    }
}
</style>