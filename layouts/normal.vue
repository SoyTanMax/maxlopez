<template>
    <div>
        <Navbar class="navbar"
            :home="home"
        />
        <Nuxt class="nuxt"/>
        <Footer />
    </div>
</template>

<script>
    import Navbar from '~/components/Navbar'
    import Footer from '~/components/Footer'
    export default {
        components: {
            Navbar,
            Footer
        },
        data() {
            return {
                home: true
            }
        },
    }
</script>

<style scoped>

.navbar{
    padding-left: 96px;
    padding-right: 96px;
    z-index: 98;
}
.nuxt{
    z-index: 99;
}
@media screen and (max-width: 769px) {
    .navbar{
        padding: 0 24px;
    }
}
</style>