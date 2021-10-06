<template>
  <div id="cv">
    
    <div class="container-row1">
      <div class="container-soft-contact">
        <div class="contact">
          <div class="title-contact"><h1>Contact</h1></div>
          <div class="container-contact transform-container">
            <div class="container-adress">
              <div class="margin-icon">
                <i class="fas fa-map-marker-alt"></i>
              </div>
              <div class="adress">Cannes, 06400</div>
            </div>
            <div class="container-mail">
              <div class="margin-icon"><i class="fas fa-at"></i></div>
              <div class="mail">
                <a id="link" href="mailto:fourquier.anthony@hotmail.fr"
                  >Fourquier.anthony@hotmail.fr</a
                >
              </div>
            </div>
            
            <div class="container-phone">
              <div class="margin-icon"><i class="fas fa-mobile-alt"></i></div>
              <div class="phone">
                <a id="link" href="tel:+0627575561">0627575561</a>
              </div>
            </div>
            <div class="container-licence">
              <div class="margin-icon"><i class="fas fa-car"></i></div>
              <div class="driving-licence">Permis A, B</div>
            </div>
            <div class="social-network">
              <div class="container-linkedin">
                <div class="margin-icon"><i class="fab fa-linkedin"></i></div>
                <div class="linkedin">
                  <a
                    id="link"
                    href="https://www.linkedin.com/in/anthony-fourquier"
                    target="_blank"
                  >
                    Linkedin Anthony Fourquier</a
                  >
                </div>
              </div>
              <div class="container-github">
                <div class="margin-icon"><i class="fab fa-github"></i></div>
                <div class="github">
                  <a
                    id="link"
                    href="https://www.github.com/AnthonyFourquier"
                    target="_blank"
                    >Github AnthonyFourquier</a
                  >
                </div>
              </div>
              <div class="facebook"></div>
            </div>
          </div>
        </div>
        <div class="softskill">
          <div class="title-softskill"><h1>Qualités</h1></div>
        
          <div class="container-softkill transform-container">
              <div class="autonomy">
                Autonome : organisé et discipliné
              </div>
              <div class="curious">
                Curieux : intérêt pour les
                nouveautés
              </div>
            
              <div class="teamwork">
                Solidaire : aider pour réussir un
                projet
              </div>
              <div class="analytic">
                Analytique : compréhension des besoins
              </div>
              <div class="adaptation">
                Adaptation : disponible et flexible
              </div>
          </div>
        </div>
      </div>

      <div class="profil ">
        <div class="title-profil"><h1>Profil</h1></div>
        <div class="container-profil md-elevation-8 transform-container">
          <div><img src="../assets/photo.png" class="photo" /></div>
          <div class="border"></div>
          <div class="synopsis">
            <div>
              <p>
                Mordu d’informatique depuis mon plus jeune âge, j’ai commencé
                par effectuer des dépannages et des installations
                d’ordinateurs.<br />
                Le domaine du web a attiré ma curiosité et m’a permis de me
                lancer dans une formation de 6 mois qui a étoffé mon panel de
                compétences.
              </p>
            </div>
          </div>
        </div>
      </div>
      <div class="formation">
        <div class="title-formation"><h1>Formations</h1></div>
        <div class="container-formation  transform-container">
          <div class="bocalacademy">
            <div class="info">
              <div><img src="../assets/bocalacademy.png" class="logo" /></div>
              <div class="name">
                Developpement web et mobile - Bocal academy, NICE
              </div>
            </div>
            <div class="programme">
              <div>
                <p>Developpement d'applications web avec base de données</p>
              </div>
              <div>
                <p>
                  Création d'application client-serveur avec interface
                  utilisateur
                </p>
              </div>
            </div>
            <div class="border"></div>
          </div>
          <div class="universite">
            <div class="info">
              <div><img src="../assets/valrose.jpg" class="logo2" /></div>
              <div class="name2">Université cote d'azur - Valrose, NICE</div>
            </div>
            <div class="programme">
              <div><p>Licence 2 informatique et mathématiques</p></div>
              <div>
                <p>Approfondissement des mathématiques et algorithmie</p>
              </div>
            </div>
            <div class="border"></div>
          </div>
          <div class="management">
            <div class="info">
              <div><img src="../assets/steaknshake.png" class="logo3" /></div>
              <div class="name3">
                Techniques de management - Steak'n Shake, MONACO
              </div>
            </div>
            <div class="programme">
              <div>
                <p>Importance de la communication et du travail d'équipe</p>
              </div>
              <div>
                <p>
                  Adaptabilité, analyse et prise de recul pour l'atteinte d'un
                  objectif
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div id='position' class="container-bar-progress">
      <div class="container-bar-progress-front">
        <div class="softskill-front"><h1>Compétences Front</h1></div>
        <div class="loading-bar" >
          <div class="position-percentage"  >{{ percentagehtml }}%</div>
          <div class="percentage" :style="{ width: percentagehtml + '%' }" >
            <div class="background_html">
              <div class="html">
                <b>HTML</b>
              </div>
            </div>
          </div>
        </div>
        <div class="loading-bar">
          <div class="position-percentage">{{ percentagecss }}%</div>
          <div class="percentage" :style="{ width: percentagecss + '%' }">
            <div class="background_html">
              <div class="html">
                <b>CSS</b>
              </div>
            </div>
          </div>
        </div>
        <div class="loading-bar">
          <div class="position-percentage">{{ percentagejs }}%</div>
          <div class="percentage" :style="{ width: percentagejs + '%' }">
            <div class="background_js">
              <div class="js"><b>Javascript</b></div>
            </div>
          </div>
        </div>
        <div class="loading-bar">
          <div class="position-percentage">{{ percentagevuejs }}%</div>
          <div class="percentage" :style="{ width: percentagevuejs + '%' }">
            <div class="background_vuejs">
              <div class="vue-js">
                <b>Vue JS</b>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="btnResp">
        <a id="link" href="../assets/FourquierAnthonyCv.pdf" download="FourquierAnthonyCv.pdf">
          <button class="download"><span>télécharger cv</span></button>
        </a>

      </div>
      <div class="container-bar-progress-back">
         <div class="softskill-back"><h1>Compétences Back</h1></div>
        <div class="loading-bar">
          <div class="position-percentage">{{ percentagephp }}%</div>
          <div class="percentage" :style="{ width: percentagephp + '%' }">
            <div class="background_php">
              <div class="php"><b>PHP</b></div>
            </div>
          </div>
        </div>
        <div class="loading-bar">
          <div class="position-percentage">{{ percentagelaravel }}%</div>
          <div class="percentage" :style="{ width: percentagelaravel + '%' }">
            <div class="background_laravel">
              <div class="laravel">
                <b>Laravel</b>
              </div>
            </div>
          </div>
        </div>
        <div class="loading-bar">
          <div class="position-percentage">{{ percentagemysql }}%</div>
          <div class="percentage" :style="{ width: percentagemysql + '%' }">
            <div class="background_html">
              <div class="html">
                <b>MySQL</b>
              </div>
            </div>
          </div>
        </div>
        <div class="loading-bar">
          <div class="position-percentage">{{ percentagewp }}%</div>
          <div class="percentage" :style="{ width: percentagewp + '%' }">
            <div class="background_js">
              <div class="js"><b>WordPress</b></div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="margin-bottom" style="height:40px"></div>
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
export default {
  name: "Cv",
 
  data: () => {
    return {
      percentagehtml: 0,
      percentagecss: 0,
      percentagephp: 0,
      percentagemysql: 0,
      percentagejs: 0,
      percentagewp: 0,
      percentagevuejs: 0,
      percentagelaravel: 0,
    };
  },
  computed: {
    percenthtml() {
      return this.percentagehtml.toFixed();
    },
    percentcss() {
      return this.percentagecss.toFixed();
    },
    percentphp() {
      return this.percentagephp.toFixed();
    },
    percentmysql() {
      return this.percentagemysql.toFixed();
    },
    percentjs() {
      return this.percentagejs.toFixed();
    },
    percentwp() {
      return this.percentagewp.toFixed();
    },
    percentvuejs() {
      return this.percentagevuejs.toFixed();
    },
    percentlaravel() {
      return this.percentagelaravel.toFixed();
    },
  },
  methods:{
    animateBarScroll() {
       let scrollValue =
        document.body.scrollTop || document.documentElement.scrollTop;
        let id = document.getElementById('position');
        let positionId = id.scrollTop ;
      if(scrollValue > positionId){
         var intval = setInterval(() => {
      if (this.percentagehtml < 85) this.percentagehtml += 1;
      else clearInterval(intval);
    }, 80);
     var intval1 = setInterval(() => {
      if (this.percentagecss < 85) this.percentagecss += 1;
      else clearInterval(intval1);
    }, 80);

    var intval2 = setInterval(() => {
      if (this.percentagephp < 75) this.percentagephp += 1;
      else clearInterval(intval2);
    }, 80);

    var intval3 = setInterval(() => {
      if (this.percentagemysql < 85) this.percentagemysql += 1;
      else clearInterval(intval3);
    }, 80);

    var intval4 = setInterval(() => {
      if (this.percentagejs < 70) this.percentagejs += 1;
      else clearInterval(intval4);
    }, 80);

    var intval5 = setInterval(() => {
      if (this.percentagewp < 75) this.percentagewp += 1;
      else clearInterval(intval5);
    }, 80);

    var intval6 = setInterval(() => {
      if (this.percentagevuejs < 70) this.percentagevuejs += 1;
      else clearInterval(intval6);
    }, 80);

    var intval7 = setInterval(() => {
      if (this.percentagelaravel < 85) this.percentagelaravel += 1;
      else clearInterval(intval7);
    }, 80);
      }
      
      if( scrollValue < 3200){
        this.percentagehtml = 0;
        this.percentagecss = 0;
        this.percentagelaravel = 0;
        this.percentagejs = 0;
        this.percentagevuejs = 0;
        this.percentagemysql = 0;
        this.percentagewp = 0;
        this.percentagephp = 0;

      }

    },
    animateCv(){
         let scrollValue =
        document.body.scrollTop || document.documentElement.scrollTop;
        let animateCvId = document.getElementById("cv");
        if(scrollValue > 2700){
          animateCvId.classList.add('animateCv');
        }
        else
        animateCvId.classList.remove('animateCv');
        
    },
     scrollListener() {
      resizeThrottler(this.animateBarScroll);
    },
      scrollListener2() {
      resizeThrottler2(this.animateCv);
    },
  }, 
    mounted() {
    document.addEventListener("scroll", this.scrollListener);
    document.addEventListener("scroll", this.scrollListener2);
  },
  beforeDestroy() {
    document.removeEventListener("scroll", this.scrollListener);
    document.removeEventListener("scroll", this.scrollListener2);
  },
  
};
</script>
<style lang="scss" scoped>
#link {
  text-decoration: none;
  color: #00314c;
}
.adaptation, .analytic, .curious, .teamwork, .autonomy{
 margin-left: 17.5%;
}
.margin-icon {
  margin-top: 5px;
  margin-left: 5% ;
}
.container-adaptation {
  display: flex;
  flex-direction: row;

}
.container-analytic {
  display: flex;
  flex-direction: row;
}
.container-curious {
  display: flex;
  flex-direction: row;
 
}
.container-autonomy {
  display: flex;
  flex-direction: row;
  
}
.container-adress {
  display: flex;
  flex-direction: row; 
}
.container-mail {
  display: flex;
  flex-direction: row;
}
.container-phone {
  display: flex;
  flex-direction: row;
  margin-left:2px;
 
}
.container-licence {
  display: flex;
  flex-direction: row;

}
.container-linkedin {
  display: flex;
  flex-direction: row;
 
}
.container-github {
  display: flex;
  flex-direction: row;

}

.container-soft-contact {
  width: 25%;
}

.container-bar-progress {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 80%;
 margin: auto;
}
.softskill-front, .softskill-back{
  padding-bottom: 10px;
}
.container-row1 {
  display: flex;
  flex-direction: row;
  width: 100%;
  justify-content: space-evenly;
  margin-bottom: 100px;
}
.profil {
  width: 25%;
}
.synopsis {

  margin-left: auto;
  padding: 10px;
}
.container-profil {
  display: flex;
  flex-direction: column;
  justify-content: center;
  border: 1px solid white;
  background-color: white;
  margin-top: 1%;
  padding: 8px;
  color: #00314c;
   transition: all 0.5s;
}
.photo {
  height: 200px;
  width: 200px;
  margin-bottom: 7.5%;
  margin-top: 5%;
}

.container-softkill {
  display: flex;
  flex-direction: column;
  border: 1px solid white;
  box-shadow: -5px 5px 5px rgba(0, 0, 0, 0.2);
  margin: auto;
  background-color: white;
  text-align: left;
  margin-top: 1%;
  padding: 10px;
  color: #00314c;
   transition: all 0.5s;
}

.container-contact {
  display: flex;
  flex-direction: column;
  border: 1px solid white;
  box-shadow: -5px 5px 5px rgba(0, 0, 0, 0.2);
  background-color: white;
  color: #00314c;
  margin-top: 1%;
  padding: 10px;
  margin-bottom: 25px;
  transition: all 0.5s;
}
.transform-container:hover{
  transform: scale(1.15);
  transition-duration: 1s;
  transition-timing-function: cubic-bezier(0.4, 0.0, 0.2, 1);  
    background-color: #00314c;
    color: white;
    border: none;
    
    #link{
  transition-duration: 1s;
  transition-timing-function: cubic-bezier(0.4, 0.0, 0.2, 1);  
      color: white;
    }
}


.autonomy,
.curious,
.teamwork,
.analytic,
.adaptation {
  
  line-height: 35px;
}
.mail,
.adress,
.phone,
.driving-licence,
.linkedin,
.github {
  margin-left: 10%;
  line-height: 25px;
}
.phone{
  padding-left: 3px;
}
.html {
  color: white;
  overflow: hidden;
  position: relative;
  top: 2px;
  font-size: 12px;
  left: 20px;
  text-align: left;
}
.background_html {
  height: 30px;
  width: 25%;
}
.php {
  color: white;
  overflow: hidden;
  position: relative;
  top: 2px;
  left: 20px;
  font-size: 12px;
  text-align: left;
}
.background_php {
  height: 30px;
  width: 25%;
}
.background_js {
  height: 30px;
  width: 40%;
}
.js {
  color: white;
  overflow: hidden;
  position: relative;
  top: 2px;
  left: 20px;
  font-size: 12px;
  text-align: left;
}
.background_vuejs {
  height: 30px;
  width: 25%;
}
.vue-js {
  color: white;
  overflow: hidden;
  position: relative;
  top: 2px;
  left: 20px;
  font-size: 12px;
  text-align: left;
}
.background_laravel {
  height: 30px;
  width: 25%;
}
.laravel {
  color: white;
  overflow: hidden;
  position: relative;
  top: 2px;
  left: 20px;
  font-size: 12px;
  text-align: left;
}
.loading-bar {
  position: relative;
  width: 300px;
  height: 25px;
  overflow: hidden;
  border-radius: 15px;
  border-bottom: 1px solid #ddd;
  border-top: 1px solid #ddd;
  box-shadow: inset 1px 1px 4px;
  margin-top: 5%;
  background: rgba(16, 13, 81, 0.1);
}

.percentage {
  position: absolute;
  top: 0px;
  left: 1px;
  right: 1px;
  display: block;
  height: 100%;
  width: 50%;
  border-radius: 15px;
  background-color: #00314c;
  background-size: 30px 30px;
  box-shadow: inset 1px 1px 4px;
  animation: animate-bar 3s linear infinite;
}
.position-percentage {
  text-align: right;
  margin-right: 10px;
  margin-top: 2px;
  font-size: 13px;

  font-weight: bold;
}
.image {
  height: 200px;
  width: 300px;
}
.experiences {
  display: flex;
  flex-direction: column;
 
}

.bocalacademy,
.universite,
.management {
  padding-right: 10px;
}
.info {
  display: flex;
  padding-top: 5px;
}
.logo {
  height: 30px;
  margin-left: 10px;
}
.name {
  margin-top: 10px;
  margin-left: 10px;
}
.name3 {
  margin-left: 3px;
  margin-top: 10px;
}
.formation {
  display: flex;
  flex-direction: column;
  
}
.container-formation {
  color: #00314c;
  background-color: white;
  box-shadow: 5px 5px 5px rgba(0, 0, 0, 0.2);
   transition: all 0.5s;
}
#cv {
  margin-top: 80px;
  width: 85%;
  margin: auto;

}
.logo2 {
  width: 60px;
}
.logo3 {
  height: 40px;
  margin-left: 8px;
}
.name2 {
  margin-left: -10px;
  margin-top: 8px;
}
.programme p {
  text-align: left;
  margin-left: 15%;
}

.border {
  border: 1px solid lightgrey;
  width: 60%;
  margin: auto;
}


button {
  display: block;
  height: 175px;
  width: 175px;
  text-decoration: none;
  text-align: center;
  position: relative;
  transition: all .1s;
  border: 2px solid #00314c;
  background-color: white;
  border-radius: 50%;
  color: #00314c;
  font-weight: bold;
  text-align: center;
  letter-spacing: 0.4px;
  text-transform: uppercase;
  cursor: pointer;
}

button span{
  position: relative;
  z-index: 2;
}

button:after{
  position: absolute;
  content: "";
  top: 0;
  left: 0;
  width: 0;
  height: 100%;
  border-radius: 50%;
  background-color: #00314c;
  transition-duration: 0.35s;
  transition-timing-function: cubic-bezier(0.4, 0.0, 0.2, 1);  
 
}

button:hover{
  color: #fff;
  border: 2px solid white;
}

button:hover:after{
  width: 100%;
}

.animateCv{
  animation: animate-cv 0.5s, animate2-cv 1s ;
  animation-timing-function: 	cubic-bezier(0.4, 0.0, 0.2, 1);
}
@keyframes animate-bar {
  0% {
    background-position: 0 0;
  }
  100% {
    background-position: 60px 0;
  }
}
@keyframes animate-cv{
  0%{
    opacity: 0;
  }
  100%{
    opacity: 1;
  }
}
@keyframes animate2-cv {
  from {
    margin-top: 100%; 
  }

  to {
    margin-top: 0%;
  }
}
@media screen and (max-width: 500px) {
  .animateCv{
  animation: no ;
  }

  #cv{
    width: 90%;
    margin: auto;
  }

  .container-row1, .container-bar-progress{
   display: flex;
   flex-direction: column;
    margin: 0;
    padding: 0;
  }
  .contact, .container-soft-contact, .container-row1, .container-contact, .container-softskill, .profil, .formation{
    width: 100%;
  
  }
  .autonomy, .curious, .analytic, .adaptation, .teamwork{
    margin-left: 7.5%;
    }
  .synopsis{
    padding: 10px;
    margin-top: 10px;
    }

 .softskill-front h1 {
    margin-left: 0;
     font-size: 20px;
     text-align: center;
     margin-top: 50px;
  }
  .softskill-back h1{
    font-size: 20px;
    width: 100%;
    text-align: center;
    margin-top: 50px;
  }
  .download{
    height: 25px;
    border-radius: 0;
    font-size: 10px;
    margin: auto;
  }
  .download:after{
     border-radius: 0;
  }
  .btnResp{
    padding-top: 50px;
  }
  .loading-bar{
    width: 100%;
    margin-left: auto;
  }
  .container-bar-progress{
   margin: auto;
  }
  .title-contact, .title-profil, .title-softskill{
    margin-left: 0;
  }
  h1{
    text-align: center;
  }
  .title-softskill, .title-profil, .title-formation{
    margin-top: 75px;
  }
  .container-formation,  p  {
    margin: 0;
    padding-bottom: 10px;
   
  }

.bocalacademy p, .universite p, .management p{
  padding-bottom: 5px;
  padding-top: 5px;
 
}
.bocalacademy .border {
  margin-top: 20px;
  margin-bottom: 15px;
}
.universite .border{
  margin-top: 20px;
  margin-bottom: 15px;
}
.name, .name2, .name3{
  padding-bottom: 15px;
 }
}
@media screen and (min-width: 501px) and (max-width: 1024px) {
  .animateCv{
  animation: no ;
  }
  #cv{
    width: 90%;
    margin: auto;
  }
  .container-row1{
   display: flex;
   flex-direction: row;
   flex-wrap: wrap;
    margin: 0;
    padding: 0;
    width: 100%;
  }
  .container-row1{
    justify-content: space-between;
    margin-top: -50px;
  }
  .container-soft-contact{
    width: 45%;
  }
  .profil{
    width: 50%;
  }
  .container-contact{
    width: 100%;
  }
  .title-formation{
    margin-left: 60%;
    margin-top: 50px;
  }
  .container-formation{
   margin-left: 32.5%;
   width: 100%;
  }
  .container-bar-progress{
    display: flex;
    flex-direction: column;
    margin: auto;
    margin-top: 50px;
  }
  .loading-bar{
    margin: auto;
    margin-top:3% ;
  }
  .softskill-front,.softskill-back{
    margin-top: 25px;
  }
  .download{
    margin: auto;
    margin-top: 25px;
  }
}
</style>
