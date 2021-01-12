<template>
    <a :href="link" class="float-bottom">
        <b-icon
            :icon="icon"
            :custom-size="size"
        >
        </b-icon>
    </a>
</template>

<script>
export default {
    name: "IconLink",
    props: {
        icon: {
            type: String
        },
        size: {
            default: "mdi-24px",
            type: String
        },
        link: {
            type: String
        }
    }
}
</script>

<style scoped lang="scss">
@import "assets/scss/main";
a {
    margin-left: 7px;
    margin-right: 7px;
    margin-bottom: 7px;
    transition: $transition-speed;
}

.float-bottom {
    margin-top: auto;
}
</style>
