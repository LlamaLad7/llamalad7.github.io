<template>
    <b-navbar class="padded is-fixed-top">
        <template #brand>
            <b-navbar-item id="name" tag="router-link" :to="{ path: '/' }">
                <p class="has-text-weight-semibold is-size-5">LlamaLad7</p>
            </b-navbar-item>
        </template>
        <template #start>
            <b-navbar-item tag="router-link" :to="{ path: '/skills' }">
                Skills
            </b-navbar-item>
            <b-navbar-item tag="router-link" :to="{ path: '/projects' }">
                Projects
            </b-navbar-item>
        </template>
    </b-navbar>
</template>

<script>
export default {
    name: "NavBar"
}
</script>

<style scoped lang="scss">
@import "assets/scss/main";
.padded {
    padding: 10px 20px 20px;
}

.navbar-item, .navbar-burger {
    color: $link;
    transition: $transition-speed;
    background-color: #fff0 !important;
}

#name:hover, .navbar-item:hover, .nuxt-link-active {
    color: $primary !important;
}

#name {
    color: $link !important;
    margin-top: -1.3px;
}
</style>
