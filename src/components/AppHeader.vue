<template>
    <header>
        <span class="title">学生评价系统</span>
        <span class="options">
            <span class="profile" @click="checkProfile">
            
                    </span>
            <span class="message" @click="showMessage">
                        <icon name="envelope-o"></icon>
                    </span>
            <span class="logout" @click="logout">
                        <icon name="sign-out"></icon>
                    </span>
        </span>
    </header>
</template>


<script>

export default {
    data() {
        return {

        }
    },
    methods: {
        logout() {
            console.log("Fire the logout methods");
        },
        checkProfile() {
            console.log("Checkout the profile.");
        },
        showMessage(){
            console.log("show me the unread messsages.");
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

header {
    height: 50px;
    width: 100%;
    background: $mauve;
    color: white;
    .title {
        margin: 0px 0px 0px 10px;
        line-height: 50px;
        font-family: $f;
        text-shadow: 1px 1px 1px #fff;
    }
    .options {
        float: right;
        height: 50px;
        display: flex;
        align-items: center;
        .profile {
            display: inline-block;
            margin-right: 20px;
            width: 30px;
            height: 30px;
            border: 1px solid white;
            border-radius: 50%;
            box-shadow: 0 0 5px #eee;
            &:hover{
                border-color: #ccc;
                cursor: pointer;
            }
        }
        .message{
            margin-right: 20px;
            &:hover {
                color: #ccc;
                cursor: pointer;
            }
        }
        .logout {
            margin-right: 20px;
            &:hover {
                color: #ccc;
                cursor: pointer;
            }
        }
    }
}
</style>
