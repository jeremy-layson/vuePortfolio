<template>
    <div class="introduction" id="introduction">
        <div class="name">
            <h1>I am {{name.first}}</h1>
        </div>
        <div class="about-me" id="about-me">
            <p>A young software developer who specializes in back-end development</p>
            <p>&nbsp;</p>
            <p>I also do front-end development and hardware integrations on my side projects.</p>
            <p>&nbsp;</p>
            <p>I like coffee, writing <span style="text-decoration: line-through;">messy</span> codes and stories.</p>
        </div>
        <div class="button-container">
            <a href="#summary-work" v-on:click="scrollDown">
                <div class="button"><p class="long-override">{{caption}}</p></div>
            </a>
        </div>
    </div>
</template>

<script>
    import $ from 'JQuery'
    export default {
        name: 'introduction',
        data() {
            return {
                caption: 'Interesting, tell me more.',
                name: {
                    first: 'Jeremy',
                    middle: 'Bondoc',
                    last: 'Layson'
                }
            }
        },
        computed: {
            commonName: function() {
                return this.name.first + ' ' + this.name.last;
            },
            fullName: function() {
                return this.name.first + ' ' + this.name.middle + ' ' + this.name.last;
            }
        },
        methods: {
            scrollDown: function(e) {
                // Make sure this.hash has a value before overriding default behavior
                if (window.location.hash !== "") {
                  // Prevent default anchor click behavior
                  e.preventDefault();

                  // Store hash
                  var hash = $(e.target).parent().attr('href');

                  // Using jQuery's animate() method to add smooth page scroll
                  // The optional number (800) specifies the number of milliseconds it takes to scroll to the specified area
                  
                  $('html, body').animate({
                    scrollTop: $(hash).offset().top
                  }, 800, function(){
               
                    // Add hash (#) to URL when done scrolling (default click behavior)
                    window.location.hash = hash;
                  });
                } // End if
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import '../assets/scss/intro.scss';
    @import '../assets/scss/r-intro.scss';
</style>
