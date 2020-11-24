<template lang="pug">
div
  cv-header
  cv-hero
  cv-proyectos#proyectos
  cv-curriculum#curriculum
  cv-footer#footer
</template>

<script>
import CvHeader from './components/CvHeader.vue'
import CvHero from './components/CvHero.vue'
import CvProyectos from './components/CvProyectos.vue'
import CvCurriculum from './components/CvCurriculum.vue'
import CvFooter from './components/CvFooter.vue'

export default {
  name: 'App',
  components: {
    CvHeader,
    CvHero,
    CvProyectos,
    CvCurriculum,
    CvFooter
  }
}
</script>

<style>
</style>
