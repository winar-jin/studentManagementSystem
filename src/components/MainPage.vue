<template>
    <div id="mainpage">
        <AppHeader></AppHeader>
        <main>
            <NavBar></NavBar>
            <SlideShow></SlideShow>
        </main>
    </div>
</template>


<script>
import AppHeader from './AppHeader';
import NavBar from './NavBar';
import SlideShow from './SlideShow';

export default {
    name: 'Hello',
    components: {
        AppHeader,
        NavBar,
        SlideShow
    },
    data() {
        return {
            
        }
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
#mainpage{
    background-color: rgba(244, 10, 10, .3);
    height: 100vh;
    width: 100vw;
    main{
        
    }
}
</style>
