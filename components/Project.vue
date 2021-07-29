<template>
    <nuxt-link :to="id" class="project">
        <img class="logo" :src="logo" alt="">
        <p class="description">{{ description }}</p>
        <img class="mock" :src="mock" alt="">
        <div v-for="tag in tags" :key="tag.id">
            <p class="tag">{{ tag }}</p>
        </div>
    </nuxt-link>
</template>

<script>
    export default {
        name: "Project",
        props: ["id", "logo","description", "mock", "tags"]
    }
</script>

<style scoped>
    .project{
        position: relative;
        display: flex;
        flex-direction: column;
        background: linear-gradient(128.04deg, #6144D9 20.86%, #44ACD9 93.86%);;
        border-radius: 12px;
        padding: 24px;
        height: 350px;
    }
    .description{
        color: white;
    }
    .logo{
        max-width: 180px;
        margin-bottom:18px;
    }
    .mock{
        position: absolute;
        width: 200px;
        right: 10px;
        bottom: 0;
    }
    .description{
        width: 150px;
    }
    .tag{
        background: #ffffff;
        margin-top: 12px;
        color: #6144D9;
        font-weight: bold;
    }

/*mobile*/
    @media screen and (max-width: 769px) {
        .logo{
            max-width: 120px;
            margin-bottom:18px;
        }
        .mock{
            position: absolute;
            width: 150px;
            right: 10px;
            bottom: 0;
        }
        .project{
            background: linear-gradient(128.04deg, #6144D9 20.86%, #44ACD9 93.86%);
            display: flex;
            flex-direction: column;
            height: 280px;
            width: 100%;
            border-radius: 12px;
            padding: 24px 18px;
        }
        .description{
            width: 150px;
        }
    }

</style>