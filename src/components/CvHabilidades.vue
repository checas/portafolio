<template lang="pug">
.section
    .columns
        .column
            h1.has-text-centered.pb-2 HTML
            progress.progress.is-success(value="90" max="100")
        .column
            h1.has-text-centered.pb-2 CSS
            progress.progress.is-success(value="80" max="100")
        .column
            h1.has-text-centered.pb-2 JavaScript
            progress.progress.is-success(value="75" max="100")
        .column
            h1.has-text-centered.pb-2 VUE
            progress.progress.is-success(value="75" max="100")
        .column
            h1.has-text-centered.pb-2 Boostrap
            progress.progress.is-success(value="80" max="100")
    .columns
        .column
            h1.has-text-centered.pb-2 Bulma
            progress.progress.is-success(value="75" max="100")
        .column
            h1.has-text-centered.pb-2 PUG
            progress.progress.is-success(value="75" max="100")
        .column
            h1.has-text-centered.pb-2 SASS
            progress.progress.is-warning(value="50" max="100")
        .column
            h1.has-text-centered.pb-2 Git
            progress.progress.is-success(value="80" max="100")
        .column
            h1.has-text-centered.pb-2 GitHub
            progress.progress.is-success(value="80" max="100")
    .columns
        .column
            h1.has-text-centered.pb-2 PHP
            progress.progress.is-warning(value="50" max="100")
        .column
            h1.has-text-centered.pb-2 Laravel
            progress.progress.is-danger(value="30" max="100")
        .column
            h1.has-text-centered.pb-2 Java
            progress.progress.is-warning(value="50" max="100")
        .column
            h1.has-text-centered.pb-2 MySQL
            progress.progress.is-success(value="75" max="100")
        .column
            h1.has-text-centered.pb-2 C++
            progress.progress.is-success(value="80" max="100")
    .columns
        .column
            h1.has-text-centered.pb-2 C#
            progress.progress.is-success(value="80" max="100")
        .column
            h1.has-text-centered.pb-2 Basic
            progress.progress.is-success(value="75" max="100")
        .column
            h1.has-text-centered.pb-2 VBA
            progress.progress.is-success(value="80" max="100")
        .column
            h1.has-text-centered.pb-2 Android Studio
            progress.progress.is-success(value="75" max="100")
        .column
            h1.has-text-centered.pb-2 Microsoft office
            progress.progress.is-success(value="90" max="100")
    .columns
        .column
            h1.has-text-centered.pb-2 AutoCad
            progress.progress.is-success(value="75" max="100")
        .column
            h1.has-text-centered.pb-2 Matlab
            progress.progress.is-success(value="75" max="100")
        .column
            h1.has-text-centered.pb-2 SCADA
            progress.progress.is-warning(value="50" max="100")
        .column
            h1.has-text-centered.pb-2 Fotografía digital
            progress.progress.is-warning(value="50" max="100")
</template>
<style scoped>
h1 {
    color: #ECE5ED;
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
}
</style>