<template>
    <div id="app">
        <h1>vue-badgen</h1>
        <a href="https://badgen.net/" target="_blank">https://badgen.net/</a>
        <p>
            demo :
        </p>
        <Badgen
            type="classic"
            subject="vue-badgen"
            status="1.0.0"
            color="blue"
        />
    </div>
</template>

<script>
import Badgen from "./components/Badgen.vue";

export default {
    name: "App",
    components: {
        Badgen,
    }
};
</script>

<style>
#app {
    text-align: center;
}
</style>
