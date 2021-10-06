<template>
  <div id="project">
    <div id="menu-project" style="height:40vh"></div>
    <div id="project-menu" style="height:100px"></div>
    <div id="animate" class="card1 ">
      <div class="card1-text transform-container">
        <div class="card1-type">PROJETS</div>
        <div class="card1-title">French Tech Cote d'Azur</div>
        <div class="card1-synopsis">
          Site de gestion pour une association recensant 75 entreprises SPA
          réalisé en Vue-js, Laravel API et MySQL
        </div>
        <div class="card1-skill">
          <ul>
            <li>Géolocalisation des entreprises</li>
            <li>Recherche en AJAX</li>
            <li>Dashboard admin</li>
            <li>Validation des comptes par un admin</li>
            <li>Import et export de fichiers excel</li>
            <li>Connexion par un magic-link</li>
          </ul>
        </div>
        <div class="card1-link"><a id="link">Voir le projet</a></div>
      </div>
      <div  class="card1-img transform-image">
        <img src="../assets/mockup_frenchtech.png" />
      </div>
    </div>
    <div id="menu-project" style="height:120px"></div>
    <div id="animate2"  class="card1 cardResp">
      <div class="card2-img transform-image">
       <!--  changer d'image mockup pr avoir la meme reso -->
        <img id="img2" src="../assets/mockup_wanderlust.png" />
      </div>
      <div class="card2-text transform-container-inverted">
        <div class="card1-type type-resp">PROJETS</div>
        <div class="card1-title">Wanderlust</div>
        <div class="card1-synopsis">
          Réseau social sur le thème des voyages Single Page Application réalisé
          en Vue-js
        </div>
        <div class="card1-skill">
          <ul>
            <li>Vue-CLI avec vue-router</li>
            <li>Web API (node-js) et fetch</li>
            <li>Edition d'un profil</li>
            <li>Publications de contenus</li>
            <li>Possibilité de commenter et liker</li>
            <li>Connection et déconnection sécurisée par un token</li>
          </ul>
        </div>
        <div class="card1-link"><a id="link">Voir le projet</a></div>
      </div>
    </div>
    <div id="menu-project" style="height:120px"></div>
    <div id="animate3" class="card1 card1-resp ">
      <div class="card1-text transform-container">
        <div class="card1-type">PROJETS</div>
        <div class="card1-title">TrelloSkill</div>
        <div class="card1-synopsis">
          Site de gestion et d'organisation de projets Réalisé en Laravel 6 avec
          MySQL
        </div>
        <div class="card1-skill">
          <ul>
            <li>Blade, Eloquent ORM</li>
            <li>Middleware Authentification</li>
            <li>Système de Collections</li>
            <li>Edition d'un profil</li>
            <li>Connexion par un cookie de session</li>
            <li>
              Cascades pour ajouter, modifier et supprimer les informations
            </li>
          </ul>
        </div>
        <div  class="card1-link"><a id="link">Voir le projet</a></div>
      </div>
      <div  class="card1-img transform-image">
        <img src="../assets/mockup_trelloskill2.png" />
      </div>
    </div>
  <div id="menu-cv" style="height:120px"> </div>
  </div>
</template>

<script>
let resizeTimeout;
function resizeThrottler(actualResizeHandler) {
  if (!resizeTimeout) {
    resizeTimeout = setTimeout(() => {
      resizeTimeout = null;
      actualResizeHandler();
    }, 66);
  }
}
let resizeTimeout2;
function resizeThrottler2(actualResizeHandler2) {
  if (!resizeTimeout2) {
    resizeTimeout2 = setTimeout(() => {
      resizeTimeout2 = null;
      actualResizeHandler2();
    }, 66);
  }
}
let resizeTimeout3;
function resizeThrottler3(actualResizeHandler3) {
  if (!resizeTimeout3) {
    resizeTimeout3 = setTimeout(() => {
      resizeTimeout3 = null;
      actualResizeHandler3();
    }, 66);
  }
}
export default {
  name: "Project",
  methods: {
    // changer les animations selon les projets et regler le probleme 
    // d'utiliser une variable pr determiner les position du porjet 2 et 3
    animateProjectScroll() {
      let scrollValue =
        document.body.scrollTop || document.documentElement.scrollTop;
      let idAnimate = document.getElementById("animate");
      let positionAnimate = idAnimate.scrollTop;
      if (positionAnimate < scrollValue) {
        idAnimate.classList.add("animation1") ;
      } else idAnimate.classList.remove("animation1");
    },
    animate2ProjectScroll() {
      let scrollValue =
        document.body.scrollTop || document.documentElement.scrollTop;
      let idAnimate1 = document.getElementById("animate2");
      if ( 1100 < scrollValue) {
        idAnimate1.classList.add("animation1");
      } else idAnimate1.classList.remove("animation1");
    },
    animate3ProjectScroll() {
      let scrollValue =
        document.body.scrollTop || document.documentElement.scrollTop;
      let idAnimate1 = document.getElementById("animate3");
      if ( 1900< scrollValue) {
       
        idAnimate1.classList.add("animation1");
      } else idAnimate1.classList.remove("animation1");
    },
    scrollListener() {
      resizeThrottler(this.animateProjectScroll);
    },
    scrollListener2() {
      resizeThrottler2(this.animate2ProjectScroll);
    },
      scrollListener3() {
      resizeThrottler3(this.animate3ProjectScroll);
    },
  },
  mounted() {
    document.addEventListener("scroll", this.scrollListener);
    document.addEventListener("scroll", this.scrollListener2);
    document.addEventListener("scroll", this.scrollListener3);
  },
  beforeDestroy() {
    document.removeEventListener("scroll", this.scrollListener);
    document.removeEventListener("scroll", this.scrollListener2);
     document.removeEventListener("scroll", this.scrollListener3);
  },
};
</script>
<style lang="scss" scoped>
.transform-image:hover{
  transform: scale(1.15);
  transition-duration: 1s;
  transition-timing-function: cubic-bezier(0.4, 0.0, 0.2, 1);  
}
.transform-container:hover{
  transform: scale(1.15);
  transition-duration: 1s;
  transition-timing-function: cubic-bezier(0.4, 0.0, 0.2, 1);  
    background-color: #00314c;
    color: white;
    border: none;
    
    .card1-type, .card1-skill{
  transition-duration: 1s;
  transition-timing-function: cubic-bezier(0.4, 0.0, 0.2, 1);  
      color: white;
    }
  #link{
  transition-duration: 1s;
  transition-timing-function: cubic-bezier(0.4, 0.0, 0.2, 1);  
      color: white;
    }
}
.transform-container-inverted:hover{
  transform: scale(1.15);
  transition-duration: 1s;
  transition-timing-function: cubic-bezier(0.4, 0.0, 0.2, 1);  
    background-color: white;
    color: #00314c;
    border: none;
    
    .card1-type, .card1-skill{
  transition-duration: 1s;
  transition-timing-function: cubic-bezier(0.4, 0.0, 0.2, 1);  
      color: #00314c;
    }
  #link{
  transition-duration: 1s;
  transition-timing-function: cubic-bezier(0.4, 0.0, 0.2, 1);  
      color: #00314c;
    }
}

#project{
  width: 80%;
  margin: auto;

  }
.card1 {
  display: flex;
  flex-direction: row;
  justify-content: center;
  opacity: 0;
 
}
.card1-text {
  width: 628px;
  height: 584px;
  display: flex;
  flex-direction: column;
  text-align: left;
  background: #ffffff;
  box-shadow: -5px 5px 5px rgba(0, 0, 0, 0.2);
  margin-top: 104px;
  z-index: 1;
   transition: all 0.5s;
}
.card1-img {
  max-width: 774.13px;
  max-height: 543px;
  margin-left: -104px;
  transition: all 0.5s;
}
.card1-type {
  font-family: Raleway;
  font-style: normal;
  font-weight: bold;
  font-size: 14px;
  line-height: 18px;
  letter-spacing: 1px;
  color: #00314c;
  padding-top: 40px;
  padding-left: 66px;
}
.card1-title {
  font-size: 36px;
  line-height: 48px;
  padding-top: 19px;
  padding-left: 66px;
}
.card1-synopsis {
  font-size: 18px;
  line-height: 35px;
  padding-top: 16px;
  padding-left: 66px;
  padding-right: 73px;
  
}
.card1-skill {
  font-weight: 600;
  font-size: 16px;
  line-height: 40px;
  color: #00314c;
  padding-left: 80px;
  padding-top: 16px;
}
.card1-link {
  text-align: right;
  padding-right: 50px;
  padding-top: 15px;
}
.card2-img {
  max-width: 774.13px;
  max-height: 543px;
  transition: all 0.5s;
}
.card2-text {
  width: 628px;
  height: 584px;
  display: flex;
  flex-direction: column;
  text-align: left;
  background: #00314c;
  box-shadow: 5px 5px 5px rgba(0, 0, 0, 0.2);
  margin-top: 104px;
  margin-left: -104px;
  z-index: 1;
  color: white;
   transition: all 0.5s;
  .card1-type {
    color: white;
  }
  .card1-skill {
    color: white;
  }
  .card1-link #link {
    color: white;
  }
}
#link {
  color: #00314c;
  font-weight: 600;
  font-size: 16px;
  font-weight: bold;
  text-decoration-thickness: 2px;
  line-height: 32px;
  letter-spacing: 0.4px;
}

.animation1 {
 animation: opacity 0.5s, slidein 1s ;
  animation-timing-function: 	cubic-bezier(0.4, 0.0, 0.2, 1);
  opacity: 1;
}

@keyframes slidein {
  from {
    margin-top: 100%; 
  }

  to {
    margin-top: 0%;
  }
}
@keyframes opacity {
  from {
    opacity: 0;
  }

  to {
   opacity: 1;
  }
}

@media screen and (max-width: 500px) {
  .animation1{
    animation: none;
  }
 .card1-resp{
    margin-bottom: -150px;
  }
  #project{
    max-width: 90%;
    margin: auto;  
  } 
    
  #menu-project{
    max-height: 0px;
  }
  #project-menu{
    max-height: 50px;
  }
  .card1 {
    display: flex;
    flex-direction: row;
    justify-content: center;
    flex-wrap: wrap;
    opacity: 1;
  }
  .card1-text{
    margin-bottom: 0;
    height: auto;
  }
  .card1-type{
    font-size: 10px;
    margin: 0;
    padding-left: 20px;
  }
  .card1-title {
    font-size: 15px;
    padding: 0 ;
    margin: 0;
    font-weight: bold;
    text-align: center;
  }
  .card1-synopsis{
    font-size: 12px;
    padding: 10px;
    margin: 0;
    line-height: 20px;
    text-align: center;
  }
  .card1-skill{
    padding: 0;
    font-size: 12px;
    line-height: 30px;
  }
  .card1-link{
    padding-top: 0;
  }
  #link{
    font-size: 12px;
    font-weight: bold;
  }
  .card1-img{
    height: auto;
    margin-bottom: 100px;
    margin-left: 0;
  }
  .card2-img{
    height: auto;
    width: auto;
  }
  #img2{
    height: auto;
    width: auto;
    }
  .cardResp{
    height: auto;
  }
  .card2-text{
    margin: 0;
    padding: 0;
    height: auto;
  }
}
@media screen and (min-width: 501px) and (max-width: 1024px) {
  .animation1{
    animation-name: none;
  }
   #project{
    max-width: 90%;
    margin: auto;  
  } 
  .card1{
    margin-top: -520px;
    flex-wrap: wrap;
  }
  .card1-text{
   height: auto;
  }
  .card1-img{
    margin-left: 0;
    height: auto;
    
  }
   .card2-img{
    height: auto;
    width: auto;
    margin-top: 460px;
  }

  .card2-text{
    margin-left: 0;
    margin-bottom: 360px;
    height: auto;
    margin-top: 0;
  }
}
</style>
