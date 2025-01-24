<template>
  <div>
    <MainBlock/>
    <ourServices/>
    <customerReviews/>
    <Projects/>
    <importantNews/>
    <Feedback/>
    <usefulArticles/>
    <Certificates/>
    <ourClients/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/header.vue';
import MainBlock from './components/mainBlock.vue';
import ourServices from './components/ourServices.vue';
import customerReviews from './components/customerReviews.vue';
import Projects from './components/projects.vue';
import importantNews from './components/importantNews.vue';
import Feedback from './components/feedback.vue';
import usefulArticles from './components/usefulArticles.vue';
import Certificates from './components/certificates.vue';
import ourClients from './components/ourClients.vue';
import Footer from './components/Footer.vue';

export default { 
  name: 'App',
  components: {
    Header,
    MainBlock,
    ourServices,
    customerReviews,
    Projects,
    importantNews,
    Feedback,
    usefulArticles,
    Certificates,
    ourClients,
    Footer
  }
}
</script>

<style lang="scss">
@use './assets/style/index.scss';
</style>

<style lang="scss" scoped>

</style>
