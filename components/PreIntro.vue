<template>
    <div class="pre-introduction">
        <div class="button-container">
            <a href="#introduction" v-on:click="hideComponent" v-if="loaded">
                <div class="button"><p>{{caption}}</p></div>
            </a>
            <a href="#" v-else>
                <div class="button"><p>Loading Awesomeness...</p></div>
            </a>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    @import '../assets/scss/intro.scss';
    @import '../assets/scss/r-intro.scss';
</style>

<script>
    import $ from 'JQuery'
    export default {
        name: 'preIntro',
        data() {
            return {
                loaded: false,
                caption: 'Who are you?',
            }
        },
        methods: {
            hideComponent: function(e) {
                $('.pre-introduction').css('opacity', '0');
                setTimeout(function() {
                    $('.pre-introduction').remove();
                }, 500);
            }
        },
        mounted: function() {
            this.loaded = true;
        }
    }
</script>