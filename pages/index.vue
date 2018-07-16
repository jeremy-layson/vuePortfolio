<template>
    <section class="container">
        <preIntro/>
        <introduction/>
        <!-- <summaryWork/> -->
        <!-- <workExperience/> -->
    </section>
</template>

<script>
import Vue from 'vue'
import Introduction from '../components/Introduction.vue'
import PreIntro from '../components/PreIntro.vue'
import WorkExperience from '../components/WorkExperience.vue'
import SummaryWork from '../components/SummaryWork.vue'
import helpers from '../components/helpers/helper.js'

const helper = {
    install() {
        Vue.helpers = helpers
        Vue.prototype.$helpers = helpers
    }
}

Vue.use(helper);

export default {
    components: {
        Introduction,
        PreIntro,
        WorkExperience,
        SummaryWork
    },
    mounted: function() {
        var hash = window.location.hash;

        if (hash !== '') {
            window.location.hash = '';
        }
    }
}

</script>

<style>
    body {
      overflow: hidden;
    }
</style>
