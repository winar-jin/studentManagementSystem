<template>
    <carousel class="slider" :navigationEnabled="true" :perPage="1">
        <slide>
            <div class="slider__item">
                <img src="../assets/img/bjfu1.jpg">
            </div>
        </slide>
        <slide>
            <div class="slider__item">
                <img src="../assets/img/bjfu2.jpg">
            </div>
        </slide>
        <slide>
            <div class="slider__item">
                <img src="../assets/img/bjfu3.jpg">
            </div>
        </slide>
        <slide>
            <div class="slider__item">
                <img src="../assets/img/bjfu4.jpg">
            </div>
        </slide>
    </carousel>
</template>


<script>
import { Carousel, Slide } from 'vue-carousel';
export default {
    data() {
        return {

        }
    },
    components: {
        Carousel,
        Slide
    },
    methods: {

    },
    computed: {

    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
$mauve: #575E71;
$heather: #4e5465;
$blush: #454b5a;
$grey: #343434;
$easeOutCubic: cubic-bezier(0.215, 0.610, 0.355, 1.000);
$f: "brandon-grotesque",
"Brandon Grotesque",
"Source Sans Pro",
"Segoe UI",
Frutiger,
"Frutiger Linotype",
"Dejavu Sans",
"Helvetica Neue",
Arial,
sans-serif;
$p: 12px;
*,
*:before,
*:after {
    box-sizing: border-box;
}

* {
    -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
    transform-style: preserve-3d;
}

*:focus {
    outline: none!important;
}

.slider {
    width: 50%;
    display: block;
    margin: 0 auto;
    .slider__item {
        img {
            // width: calc(1.6*800px);
            // height: calc(0.9*800px);
            width: 800px;
            height: 500px;
        }
    }
}
</style>
