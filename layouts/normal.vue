<template>
    <div>
        <Navbar class="navbar"/>
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
        }
    }
</script>

<style scoped>

.navbar{
    padding: 0 24px;
    z-index: 98;
}
.nuxt{
    z-index: 99;
}

</style>