<template lang="pug">
.section
    h1.title Proyectos
    .tabs
        ul
            li(:class="freelanceClass")
                a(@click="freelanceSelect") Freelance
            //- li(:class="propiosClass")
            //-     a(@click="propiosSelect") Propios
            li(:class="cursosClass")
                a(@click="cursosSelect") De cursos
    cv-freelance(v-show="showFreelance")
    cv-propios(v-show="showPropios")
    cv-de-cursos(v-show="showDeCursos")
</template>

<script>
import CvFreelance from '../components/CvFreelance.vue'
import CvPropios from '../components/CvPropios.vue'
import CvDeCursos from '../components/CvDeCursos.vue'
export default {
    name: 'Proyectos',
    components: { CvFreelance, CvPropios, CvDeCursos },
    data () {
        return {
            freelanceClass: 'is-active',
            propiosClass: '',
            cursosClass: '',
            showFreelance: true,
            showPropios: false,
            showDeCursos: false
        }
    },
    methods: {
        freelanceSelect () {
            this.freelanceClass = 'is-active';
            this.propiosClass = '';
            this.cursosClass = '';
            this.showFreelance = true;
            this.showPropios = false;
            this.showDeCursos = false;
        },
        propiosSelect () {
            this.freelanceClass = '';
            this.propiosClass = 'is-active';
            this.cursosClass = '';
            this.showFreelance = false;
            this.showPropios = true;
            this.showDeCursos = false;
        },
        cursosSelect () {
            this.freelanceClass = '';
            this.propiosClass = '';
            this.cursosClass = 'is-active';
            this.showFreelance = false;
            this.showPropios = false;
            this.showDeCursos = true;
        },
    }
}
</script>
<style scoped>
.tabs li.is-active a {
    border-color: red;
    color: red;
}
@media screen and (max-width: 767px) {
    h1.title {
        text-align: center;
    }
}
</style>