<template>
<Home/>
  <Navbar/>
  <About/>
  <Resume/>
  <Skills/>
  <Projects/>
  <Testimonials/>
  <Contact/>
  <Footer/>
</template>

<script>
import Home from './components/Home.vue'
import Navbar from './components/Navbar'
import About from './components/About'
import Resume from './components/Resume'
import Skills from './components/Skills'
import Projects from './components/Projects'
import Testimonials from './components/Testimonials'
import Contact from './components/Contact'
import Footer from './components/Footer.vue'




export default {
  name: 'App',
  components: {
    Home,
    Navbar,
    About,
    Resume,
    Skills,
    Projects,
    Testimonials,
    Contact,
    Footer
    
  }
}
</script>

<style>
:root{
    scroll-behavior: smooth;
}
.home-img{
    padding-left: 3em;
    padding-right: 3em;
}
.text-blue{
    color: dodgerblue;
}
.bg-blue{
    background: dodgerblue;
    border-radius: 50%;
}
@media screen and (min-width: 768px){
    .home-img{
        padding-left: 2em;
        padding-right: 2em;
    }
}
</style>
