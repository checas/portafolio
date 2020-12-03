<template lang="pug">
.section.principal
    h1.title Proyectos
    .tabs
        ul
            li(:class="freelanceClass")
                a.title.is-5(@click="freelanceSelect") Freelance
            //- li(:class="propiosClass")
            //-     a(@click="propiosSelect") Propios
            li(:class="cursosClass")
                a.title.is-5(@click="cursosSelect") De cursos
    transition(name="fade")
        div(v-show="showFreelance")
            cv-freelance
    cv-propios(v-show="showPropios")
    transition(name="fade")
        div(v-show="showDeCursos")
            cv-de-cursos
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
.principal{
    background-color: #2D1062
}
h1 {
    color: #ECE5ED;
}
li a {
    color: #CCAEE0;
    border-color: #B30189;
}
.tabs ul {
    border-color: #B30189;
}
.tabs ul:hover {
    border-color: #B30189;
}
.tabs li.is-active a {
    border-color: #ECE5ED;
    color: #ECE5ED;
}
.tabs li a:hover{
    color:#B30189;
}
.fade-enter-active, .fade-leave-active {
    transition: opacity .2s
}
.fade-enter, .fade-leave-to {
    opacity: 0
}
@media screen and (max-width: 767px) {
    h1.title {
        text-align: center;
    }
}
</style>