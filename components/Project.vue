<template>
    <div class="card">
        <header class="card-header">
            <p class="card-header-title has-text-white">{{ title }}</p>
        </header>
        <div class="card-content">
            <div class="content">
                {{ description }}
            </div>
        </div>
        <footer class="card-footer">
            <slot/>
        </footer>
    </div>
</template>

<script>
export default {
    name: "Project",
    props: ['title', 'description']
}
</script>

<style scoped>
.card-footer {
    padding: calc(0.75rem - 7px) calc(1rem - 7px);
    margin-top: -0.5rem;
}

.card {
    display: flex;
    flex-direction: column;
    width: 100%;
}

.card-footer {
    flex-grow: 1;
}
</style>
