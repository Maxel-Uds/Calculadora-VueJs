<template>
  <div id="app">
    <Calculator @onError="showError"/>
  </div>
</template>

<script>
import Calculator from "./main/Calculator.vue"

export default {
    components: { Calculator },
    methods: {
        showError(error) {
            alert(`An error ocurred: ${error}`)
        }
    }
}
</script>

<style>
    @font-face {
        font-family: "RobotoMono";
        src: url("./fonts/RobotoMono-Thin.ttf");
    }

    * {
        font-family: "RobotoMono";
    }

    body {
        margin: 0;
    }

    #app {
        display: flex;
        flex-direction: column;
        height: 100vh;
        justify-content: center;
        align-items: center;
        text-align: center;
        color: #ffff;
        background: linear-gradient(to right, rgb(83,105,118), rgb(41, 46, 73));
    }
</style>