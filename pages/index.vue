<template>
  <div class="home">
    <Hero />
    <Categories />
    <Filters />
    <Projects />
    <Formlink />
    <Footer />
  </div>
</template>

<script>
import Hero from '~/components/Hero'
import Categories from '~/components/Categories'
import Filters from '~/components/Filters'
import Projects from '~/components/Projects'
import Formlink from '~/components/Formlink'
import Footer from '~/components/Footer'

export default {
  components: {
    Hero,
    Categories,
    Filters,
    Projects,
    Formlink,
    Footer
  },
  head(){
    return {
      title: 'Encuentra tu causa'
    }
  }
}
</script>

<style>
</style>
