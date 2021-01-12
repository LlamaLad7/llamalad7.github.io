<template>
    <div class="has-text-centered v-center">
        <p class="title is-2 has-text-primary has-text-weight-bold">LlamaLad7</p>
        <p class="is-size-4 has-text-light" id="dev">Developer</p>

        <div id="buttons">
            <IconLink icon="github" link="http://github.com/LlamaLad7" size="mdi-36px"/>
            <IconLink icon="twitter" link="https://twitter.com/Lad7Llama" size="mdi-36px"/>
            <IconLink icon="email" link="mailto:l3gomindstorms@gmail.com" size="mdi-36px"/>
        </div>
    </div>
</template>

<script>
import IconLink from "~/components/IconLink";
export default {
    name: "index",
    components: {IconLink}
}
</script>

<style scoped lang="scss">
@import "assets/scss/main";

.v-center {
    margin-top: 35vh;
}

.padded {
    width: 90px;
    margin-left: 5px;
    margin-right: 5px;
}

#buttons {
    margin-top: 20px;
}

#dev {
    margin-top: -20px;
}
</style>
