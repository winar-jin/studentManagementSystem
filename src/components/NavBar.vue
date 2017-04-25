<template>
    <nav id="menu">
        <ul>
            <li>
                <a @click="toggleSubMenu">
                    <icon name="user-o"></icon>
                    <span>课程评分</span>
                    <icon v-if="showSubMenuflag" class="rightToggle" name="caret-down"></icon>
                    <icon v-else="showSubMenuflag" class="rightToggle" name="caret-left"></icon>
                </a>
                <!--<transition name="fade" mode="out-in" appear>-->
                <ul class="subMenu">
                    <li><a><span>课程一</span></a></li>
                    <li><a><span>课程一</span></a></li>
                    <li><a><span>课程一</span></a></li>
                </ul>
                <!--</transition>-->
            </li>
        </ul>
    </nav>
</template>


<script>

export default {
    data() {
        return {
            showSubMenuflag: true
        }
    },
    methods: {
        toggleSubMenu(event) {
            event.stopPropagation();
            event.preventDefault();
            document.querySelector('.subMenu').classList.toggle('show');
            this.showSubMenuflag = !this.showSubMenuflag;
        }
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

#menu {
    margin-top: 50px;
    background-color: $mauve;
    padding: 0px 0;
    z-index: 10;
    width: 200px;
    color: white;
    -webkit-transition: all 1s ease;
    -moz-transition: all 1s ease;
    transition: all 1s ease;
    opacity: 1;
    font-family: $f;
    ul {
        list-style: none;
        margin-top: 0;
        padding: 0;
        a {
            &:hover,
            &.active {
                background-color: $heather; // border-left-color: #eee;
                color: #eee;
            }
        }
        li {
            position: relative;
            z-index: 20;
            border-bottom: 1px solid #ccc;
            padding-left: 5px;
            a {
                color: inherit;
                font-size: 16px;
                display: block;
                padding: 8px 0 8px 7px;
                text-decoration: none;
                -webkit-transition: all 1s ease;
                -moz-transition: all 1s ease;
                transition: all 1s ease;
                font-weight: 600;
                &.active+ul {
                    display: block;
                }
                span {
                    margin-left: 10px;
                }
                .rightToggle {
                    float: right;
                    margin-right: 20px;
                    margin-top: 2px;
                }
            }
            ul {
                margin-top: 0;
                display: none;
                &.show {
                    display: block;
                }
                li {
                    border-bottom: none;
                    a {
                        padding-left: 25px;
                        &:hover {
                            background-color: $blush;
                        }
                    }
                }
            }
        }
    }
}
</style>
