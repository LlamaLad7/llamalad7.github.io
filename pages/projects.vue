<template>
    <div class="content">
        <p class="title is-size-1 has-text-centered has-text-white">Projects</p>
        <div class="columns is-multiline is-centered">
            <div v-for="project in projects" class="column is-4">
                <Project
                    :title="project.title"
                    :description="project.description"
                >
                    <IconLink v-for="link in project.links" :icon="link.icon" :link="link.link"/>
                </Project>
            </div>
        </div>
    </div>
</template>

<script>
import Project from "~/components/Project";
import IconLink from "~/components/IconLink";
export default {
    name: "projects",
    components: {IconLink, Project},
    data() {
        return {
            projects: [
                {
                    title: "Pseudo",
                    description: "Dynamically-typed JVM programming language designed to be easily readable and helpful as an introduction into programming. Built from the ground up with Kotlin, ANTLR and ASM.",
                    links: [
                        {
                            icon: "github",
                            link: "https://github.com/LlamaLad7/pseudo-kt"
                        }
                    ]
                },
                {
                    title: "Sk1er LLC",
                    description: "I have been working as a Java and Kotlin developer for Sk1er LLC since October 2020, helping to create a wide variety of popular Minecraft mods and frameworks which collectively attract over 300,000 unique users each week.",
                    links: [
                        {
                            icon: "earth",
                            link: "https://sk1er.club/"
                        },
                        {
                            icon: "twitter",
                            link: "https://twitter.com/Sk1erLLC"
                        },
                        {
                            icon: "github",
                            link: "https://github.com/Sk1erLLC"
                        }
                    ]
                },
                {
                    title: "Better Chat",
                    description: "Popular Minecraft Forge mod to enhance the general look and feel of the Chat GUI.",
                    links: [
                        {
                            icon: "earth",
                            link: "https://www.curseforge.com/minecraft/mc-mods/better-chat"
                        },
                        {
                            icon: "github",
                            link: "https://github.com/LlamaLad7/Better-Chat"
                        }
                    ]
                }
            ].sort((a, b) => a.name > b.name ? 1 : -1)
        }
    }
}
</script>

<style scoped>
.content {
    margin-top: 20vh;
}

.column {
    display: flex;
}
</style>
