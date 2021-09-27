<template>
  <div id="home">
    <div id="home1" style=""></div>
    <img src="../assets/wallpaper.png" id="img" />
    <img src="../assets/name.png" id="name" />
    <Footer />
    <Project />
    <Cv />
    <About />
    <Freelance />
    
  </div>
</template>

<script>
import Cv from "@/components/Cv.vue";
import Project from "@/components/Project.vue";
import About from "@/components/About.vue";
import Freelance from "@/components/Freelance.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "Home",

  components: {
    Cv,
    Project,
    About,
    Freelance,
    Footer
    
  },

};
</script>
<style scoped>

  #img {
    position: absolute;
    left: 0;
    top: 0;
  }
  #name {
    position: relative;
    left: 0;
    top: 150px;
    width: 80%;
  }

@media screen and (max-width: 500px) {
  #home{
    max-width: 375px;
  }
  #img{
    max-width: 375px;
  }
  #name{
    display: none;
  } 
}
@media screen and (min-width: 501px) and (max-width: 1024px) {
  #home{
    max-width: 100%;
  }
  #img {
    position: absolute;
    left: 0;
    top: 0;
  }
  #name {
    position: relative;
    left: 0;
    top: 110px;
    width: 80%;
  }
}
</style>
