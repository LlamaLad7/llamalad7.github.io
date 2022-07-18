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
                    description: "I worked as a Senior Java and Kotlin developer for Sk1er LLC from October 2020 to July 2022, helping to create a wide variety of popular Minecraft mods and frameworks which collectively attract over 300,000 unique users each week.",
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
                },
                {
                    title: "Essential",
                    description: "From its release until July 2022 I was a Java and Kotlin developer for Essential: the ultimate enhancement mod for your Minecraft Java experience. It is available on both Forge and Fabric for a variety of versions from 1.8.9 to the latest.",
                    links: [
                        {
                            icon: "earth",
                            link: "https://essential.gg"
                        },
                        {
                            icon: "twitter",
                            link: "https://twitter.com/essentialmod"
                        }
                    ]
                },
                {
                    title: "MixinExtras",
                    description: "I develop MixinExtras: a companion library to SpongePowered's popular framework Mixin which aims to make writing mixins more expressive and compatible for everyone. It is used by a wide variety of developers across all versions and mod loaders.",
                    links: [
                        {
                            icon: "github",
                            link: "https://github.com/LlamaLad7/MixinExtras/"
                        }
                    ]
                },
                {
                    title: "Lunar Client",
                    description: "Since July 2022 I have been working as a Software Engineer for Moonsworth LLC, helping to create Lunar Client. I primarily work on our version independent modding platform, helping support versions all the way from 1.7 to the latest. We routinely serve over 100,000 concurrent users.",
                    links: [
                        {
                            icon: "earth",
                            link: "https://lunarclient.com/"
                        },
                        {
                            icon: "twitter",
                            link: "https://twitter.com/lunarclient/"
                        },
                        {
                            icon: "github",
                            link: "https://github.com/LunarClient/"
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
