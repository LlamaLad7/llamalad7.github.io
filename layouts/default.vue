<template>
    <div class="container">
        <NavBar/>
        <section class="main-content columns">
            <div class="container column is-11">
                <nuxt/>
            </div>
        </section>
    </div>
</template>

<style lang="scss">
html {
    overflow-y: auto !important;
}
</style>

<script>
import NavBar from "~/components/NavBar";

export default {
    components: {NavBar}
}
</script>
