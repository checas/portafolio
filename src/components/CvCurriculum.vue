<template lang="pug">
.section
    .container
        h1.title.has-text-white-bis Curriculum
        .tabs
            ul
                li(:class="antecedentesClass")
                    a.has-text-white-ter(@click="antecedentesSelect") Antecedentes laborales
                li(:class="habilidadesClass")
                    a.has-text-white-ter(@click="habilidadesSelect") Habilidades
                li(:class="estudiosClass")
                    a.has-text-white-ter(@click="estudiosSelect") Estudios
                li(:class="cursosClass")
                    a.has-text-white-ter(@click="cursosSelect") Cursos
        cv-antecedentes(v-show="showAntecedentes")
        cv-habilidades(v-show="showHabilidades")
        cv-estudios(v-show="showEstudios")
        cv-cursos(v-show="showCursos")
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
.section {
    background-color: #242424;
}
.tabs li.is-active a {
    border-color: red;
    color: red !important;
}
@media screen and (max-width: 767px) {
    h1.title.has-text-white-bis {
        text-align: center;
    }
}
</style>