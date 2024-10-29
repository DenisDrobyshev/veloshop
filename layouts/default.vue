<template>
  <div>
    <Header />
    <nuxt :key="$route.fullPath" />
    <Footer />
  </div>
</template>

<script>
import Header from '@/components/header/header'
import Footer from '@/components/footer/footer'

export default {
    name: "default",
    components: {
        Header,
        Footer
    }
};
</script>

<style lang="scss">
.page-main {
  position: relative;
  z-index: $zMain;
}
</style>
