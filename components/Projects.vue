<template>
    <div class="projects section">
        <p class="title">Latest projects</p>
        <div class="projects-container">
            <div v-for="project in projects" :key="project.id">
                <Project 
                    :id="project.id"
                    :logo="project.logo"
                    :description="project.description"
                    :mock="project.mock"
                    :tags="project.tags"
                />
            </div>
        </div>
    </div>
</template>

<script>
    import Project from '~/components/Project'
    export default {
        components:{
            Project
        },
        data() {
            return {
                projects: [
                    {id: "taconomics", logo: require('~/assets/Logo.svg'), description: "An NFT art gallery for taco-related art.", mock: require('~/assets/mock1.svg'), tags: ["UX/UI Design"]},
                    {id: "tucausa", logo: require('~/assets/Logo4.svg'), description: "A PWA to find and save your favorite pokémons.", mock: require('~/assets/mock2.svg'), tags: ["UX/UI Design", "Web development"]},
                    {id: "pokedex", logo: require('~/assets/Logo3.svg'), description: "A web platform for students to enroll in social service projects.", mock: require('~/assets/mock3.svg'),  tags: ["UX/UI Design", "Web development"]}
                ]
            }
        }
    }
</script>

<style scoped>
    .section{
        background: white;
        font-family: 'Nunito', sans-serif;
        padding-right: 96px;
        padding-left: 96px;
    }
    .projects-container{
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
        gap: 48px;
        padding: 24px 0 0;
        font-family: 'Nunito', sans-serif;
    }
    
    @media screen and (max-width: 769px) {
        .section{
            display: flex;
            justify-content: center;
            flex-direction: column;
            padding-right: 24px;
            padding-left: 24px;
        }
        .projects-container{
            display: flex;
            flex-direction: column;
        }
    }
</style>