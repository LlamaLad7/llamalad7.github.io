<template>
    <div class="content">
        <p class="title is-size-1 has-text-centered has-text-white">Languages</p>
        <div class="columns is-multiline is-centered">
            <div v-for="language in languages" class="column is-3">
                <Project :title="language.name" :description="language.description">
                    <IconLink :icon="language.icon" :link="language.link"/>
                </Project>
            </div>
        </div>

        <br>
        <p class="title is-size-1 has-text-centered has-text-white">Frameworks</p>
        <div class="columns is-multiline is-centered">
            <div v-for="framework in frameworks" class="column is-3">
                <Project :title="framework.name" :description="framework.description">
                    <IconLink :icon="framework.icon" :link="framework.link"/>
                </Project>
            </div>
        </div>

        <br>
        <p class="title is-size-1 has-text-centered has-text-white">Tools</p>
        <div class="columns is-multiline is-centered">
            <div v-for="tool in tools" class="column is-3">
                <Project :title="tool.name" :description="tool.description">
                    <IconLink :icon="tool.icon" :link="tool.link"/>
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
            languages: [
                {
                    name: "C++",
                    description: "C++ is a general-purpose programming language with object-oriented, generic, and functional features, in addition to facilities for low-level memory manipulation.",
                    icon: "book-variant-multiple",
                    link: "https://en.cppreference.com/w/"
                },
                {
                    name: "CSS",
                    description: "CSS is a style sheet language used for describing the presentation of a document written in a markup language such as HTML.",
                    icon: "book-variant-multiple",
                    link: "https://developer.mozilla.org/en-US/docs/Web/CSS"
                },
                {
                    name: "HTML",
                    description: "HTML is the standard markup language for documents designed to be displayed in a web browser.",
                    icon: "book-variant-multiple",
                    link: "https://developer.mozilla.org/en-US/docs/Web/HTML"
                },
                {
                    name: "Java",
                    description: "Java is a cross-platform, class-based, object-oriented programming language, intended to let application developers write once, run anywhere.",
                    icon: "earth",
                    link: "https://java.com/"
                },
                {
                    name: "JavaScript",
                    description: "JavaScript is a high-level, often just-in-time compiled, and multi-paradigm programming language, primarily used in frontend and backend web development.",
                    icon: "book-variant-multiple",
                    link: "https://developer.mozilla.org/en-US/docs/Web/JavaScript"
                },
                {
                    name: "Kotlin",
                    description: "Kotlin is a cross-platform, statically typed, general-purpose programming language for the JVM, complete with type inference and full Java interoperability.",
                    icon: "earth",
                    link: "https://kotlinlang.org/"
                },
                {
                    name: "Python",
                    description: "Python is an interpreted, high-level and general-purpose programming language, often used for Data Science and Machine Learning.",
                    icon: "earth",
                    link: "https://www.python.org/"
                }
            ].sort((a, b) => a.name > b.name ? 1 : -1),
            frameworks: [
                {
                    name: "Exposed",
                    description: "Exposed is a lightweight ORM framework for Kotlin. It includes a typesafe SQL wrapping DSL and lightweight data access objects.",
                    icon: "github",
                    link: "https://github.com/JetBrains/Exposed"
                },
                {
                    name: "Fabric",
                    description: "Fabric is a lightweight, experimental modding toolchain for Minecraft.",
                    icon: "earth",
                    link: "https://fabricmc.net/"
                },
                {
                    name: "Forge",
                    description: "Forge is a popular Minecraft modding API for both clients and servers.",
                    icon: "github",
                    link: "https://github.com/MinecraftForge/MinecraftForge"
                },
                {
                    name: "Ktor",
                    description: "Ktor is an asynchronous framework for creating microservices, web applications and more, in Kotlin.",
                    icon: "earth",
                    link: "https://ktor.io/"
                },
                {
                    name: "ObjectWeb ASM",
                    description: "ASM is an all purpose Java bytecode manipulation and analysis framework, used to modify existing classes or to dynamically generate new classes, directly in binary form.",
                    icon: "earth",
                    link: "https://asm.ow2.io/"
                },
                {
                    name: "React",
                    description: "React is a declarative, component-based JavaScript library for building user interfaces.",
                    icon: "earth",
                    link: "https://reactjs.org/"
                },
                {
                    name: "Vue",
                    description: "Vue is a progressive front end JavaScript framework for building user interfaces and single-page applications.",
                    icon: "earth",
                    link: "https://vuejs.org/"
                }
            ].sort((a, b) => a.name > b.name ? 1 : -1),
            tools: [
                {
                    name: "IntelliJ IDEA",
                    description: "IntelliJ is a cross-platform and market-leading JetBrains IDE for Java and Kotlin development.",
                    icon: "earth",
                    link: "https://www.jetbrains.com/idea/"
                },
                {
                    name: "PyCharm",
                    description: "PyCharm is a cross-platform JetBrains IDE for Python development.",
                    icon: "earth",
                    link: "https://www.jetbrains.com/pycharm/"
                },
                {
                    name: "CLion",
                    description: "CLion is a cross-platform JetBrains IDE for C and C++ development.",
                    icon: "earth",
                    link: "https://www.jetbrains.com/clion/"
                },
                {
                    name: "WebStorm",
                    description: "WebStorm is a cross-platform JetBrains IDE for frontend and backend web development.",
                    icon: "earth",
                    link: "https://www.jetbrains.com/webstorm/"
                },
                {
                    name: "Gradle",
                    description: "Gradle is a build automation tool for multi-language software development, including Java (Kotlin, Groovy, Scala) , C/C++, JavaScript.",
                    icon: "earth",
                    link: "https://gradle.org/"
                },
                {
                    name: "Git",
                    description: "Git is the world's most popular distributed version control system.",
                    icon: "earth",
                    link: "https://git-scm.com/"
                },
                {
                    name: "GitHub",
                    description: "GitHub is the world's most popular Git hosting service.",
                    icon: "earth",
                    link: "https://github.com/"
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
