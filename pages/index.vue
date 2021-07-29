<template>
  <div class="home">
    <Hero />
    <Projects />
    <Footer />
  </div>
</template>

<script>
import Navbar from '~/components/Navbar'
import Hero from '~/components/Hero'
import Projects from '~/components/Projects'
import Footer from '~/components/Footer'
export default {
  components: {
    Navbar,
    Hero,
    Projects,
    Footer
    
  },
  head(){
    return {
      title: "Freelance UX/UI Designer and Frontend Web Developer"
    }
  },
  data () {
    return {
      heading: "Let's design things to work as they should.",
      projects: []
    }
  }
  }
</script>

<style>
/* helpers */
.center{
  display: flex;
  justify-content: center;
  align-items: center;
}
/* desktop */
.home{
  position: relative;
  font-family: 'Nunito', sans-serif;
  overflow: hidden;
  background: linear-gradient(180deg, rgba(237, 242, 247, 0) 28.65%, #EDF2F7 66.15%);
}
.hero{
  height: 100vh;
  padding-right: 96px;
  padding-left: 96px;
}
.hero-body{
  padding: 48px 0 48px 0;
}
.heading{
  font-size: 36px;
  font-family: 'Oswald', sans-serif;
  line-height: 60px;
  color: #000000;
  font-weight: bold;
  margin: 52px 0 32px 0;
  animation-name: appear;
  animation-timing-function: ease-in;
  animation-duration: 1s;
}
.columns{
  margin-top: 48px;
}
.mywork{
  font-size: 20px;
  padding: 24px 32px;
  border-radius: 10px;
  background: linear-gradient(90deg, #26AED9 -9.85%, #3173B4 116.29%);
  color: white;
  font-weight: bold;
  margin-bottom: 24px;
  border: none;
  animation-name: appear;
  animation-timing-function: ease-in;
  animation-duration: 1s;
  animation-delay: 0.4s;
  transition: 300ms;
}
.mywork:hover{
  color: white;
  transform: scale(1.03);
}
.section{
  padding-right: 96px;
  padding-left: 96px;
}
.projects{
  padding-top: 24px;
}
.cases-container{
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 24px;
    padding: 24px 0;
    font-family: 'Nunito', sans-serif;
}
.experiments-container{
  position:relative;
  background: linear-gradient(136.42deg, #2C66A0 0%, #1AB4E6 100%);
  padding-right: 96px;
  padding-left: 96px;
  position: relative;
}
/* mobile */
@media screen and (max-width: 769px) {
  
  .columns{
    display:flex;
    flex-direction: column-reverse;
    margin-top: 0;
  }
  .button{
    font-size: 24px;
    padding: 28px 38px;
    border-radius: 10px;
    margin-bottom: 0;
    animation-name: appear;
    animation-timing-function: ease-in;
    animation-duration: 0.8s;
    animation-delay: 0.4s;
  }
  .section{
    padding-right: 24px;
    padding-left: 24px;
  }
}
/* keyframes */
@keyframes float{
  from{transform: translate(0px, 0px)}
  65%{transform: translate(20px, 50px);}
  to{transform: translate(0px, 0px)}
}
@keyframes float2{
  from{transform: translate(0px, 0px)}
  65%{transform: translate(-50px, -80px);}
  to{transform: translate(0px, 0px)}
}
@keyframes appear {
  0%{
    opacity: 0;
    transform: translateY(-20px);
    visibility: hidden;
  }
  100%{
    opacity: 1;
    transform: translateY(0px);
    visibility: visible;
  }
}
</style>
