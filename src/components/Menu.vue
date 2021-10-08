<template>
  <div class="page-container">
    <md-toolbar
      id="toolbar"
      class="md-large md-dense md-transparent "
      :class="extraNavClasses"
      :color-on-scroll="colorOnScroll"
      style="position: fixed; top: 0;"
    >
      <div class="md-toolbar-row">
        <div class="md-toolbar-section-start ">
          <span class="md-title " style="color:white">Portfolio</span>
        </div>
      </div>

      <div class="md-toolbar-row " >
        <md-tabs class="md-primary md-transparent md-resp">
          <md-tab class="btnResp" id="tab-home" md-label="Home" href="#home1"></md-tab>

          <md-tab
            id="tab-Projets"
            md-label="Projets"
            href="#project-menu"
          ></md-tab>
          <md-tab id="tab-cv" md-label="CV" href="#cv" ></md-tab>
         <!--  <md-tab id="tab-Contact " md-label="Contact" href="#about"></md-tab> -->
             
        </md-tabs>
        <md-button
            class=" md-raised md-icon-button md-dense md-transparent position"
            @click="showDialog = true"
           
          >
            <i class="fas fa-user  "></i>
          </md-button>
        <div>
          <md-dialog :md-active.sync="showDialog">
            <div  class="modalContent"
            
              style="height:50px ; padding-top:12px ; padding-bottom:10px "
            >
              <md-dialog-title   style="margin-left:35% "
                >Se Connecter</md-dialog-title
              >
            </div>
            <div style="width:550px">
              <div style="width:90% ; margin-left:5% ; margin-top:4%">
                <md-field md-clearable>
                  <label>Mail</label>
                  <md-input v-model="initial"></md-input>
                </md-field>

                <md-field>
                  <label>Password</label>
                  <md-input v-model="password" type="password"></md-input>
                </md-field>
              </div>
            </div>
            <md-dialog-actions style="margin:auto">
              <md-button style=" color:#00314c" @click="showDialog = false"
                ><b>CONNECTION</b></md-button
              >
              <md-button style=" color:#00314c" @click="showDialog = false"
                ><b>S'INSCRIRE</b></md-button
              >
            </md-dialog-actions>
            <div class="border"></div>
            <div style="margin:auto ; padding-bottom:10px;">
              <md-button style=" color:#00314c" @click="showDialog = false"
                ><b>QUITTER</b></md-button
              >
            </div>
          </md-dialog>
        </div>
      </div>
    </md-toolbar>
    <md-content>
      
      <router-view></router-view>
     
    </md-content>
  </div>
</template>

<script>
let resizeTimeout;
function resizeThrottler(actualResizeHandler) {
  // ignore resize events as long as an actualResizeHandler execution is in the queue
  if (!resizeTimeout) {
    resizeTimeout = setTimeout(() => {
      resizeTimeout = null;
      actualResizeHandler();
      // The actualResizeHandler will execute at a rate of 15fps
    }, 66);
  }
}

export default {
  name: "Menu",
  props: {
    type: {
      type: String,
      default: "primary",
      validator(value) {
        return [
          "black",
          "default",
          "primary",
          "danger",
          "success",
          "warning",
          "info",
        ].includes(value);
      },
    },
    colorOnScroll: {
      type: Number,
      default: 550,
    },
  },
  data: () => ({
    menuVisible: false,
    showDialog: false,
    initial: null,
    password: null,
    extraNavClasses: "",
    oldScroll: 0,
    show: false
  }),

  methods: {
    handleScroll() {
      let scrollValue =
        document.body.scrollTop || document.documentElement.scrollTop;
      let navbarColor = document.getElementById("toolbar");
      if ( scrollValue > this.colorOnScroll) {
        navbarColor.classList.remove("md-transparent");
        navbarColor.style.backgroundColor = "#00314c";
      } else {
        if (this.extraNavClasses) {
          this.extraNavClasses = "";
        }
        navbarColor.style.backgroundColor = "transparent";
      }
      let navbarFirstChild = document.querySelector(
        "#toolbar .md-toolbar-row:first-child"
      );

      if (this.oldScroll < scrollValue) {
        navbarFirstChild.style.height = "0";
        navbarFirstChild.style.minHeight = "0";
        document.getElementById("toolbar").style.height = "48px";
        document.getElementById("toolbar").style.minHeight = "48px";
      } else {navbarFirstChild.style.height = "48px";
         document.getElementById("toolbar").style.height = "96px";
        document.getElementById("toolbar").style.minHeight = "96px"; 
      }
      this.oldScroll = scrollValue;
    },
 
    scrollListener() {
      resizeThrottler(this.handleScroll);
    },
  },

  mounted() {
    document.addEventListener("scroll", this.scrollListener);
  },
  beforeDestroy() {
    document.removeEventListener("scroll", this.scrollListener);
  },
};
</script>

<style lang="scss" scoped>

  .position{
    position: absolute;
    right: 0;
    }

  .md-field.md-theme-default:before{
    background-color: #00314c;
  }
  .md-field.md-theme-default.md-focused label{
    color: #00314c; 
  }
  .modalContent{
  background-color: #00314c;
  color: white;
  }
  .textColor{
    color: #00314c;
  }
  .md-content.md-theme-default {
    background-color: #f1f1f1;
    color: #00314c;
  }
  .md-dialog .md-dialog-container {
    max-width: 768px;
  }
  .md-field:last-child {
    margin-bottom: 40px;
  }
  .border {
    margin-top: 2%;
    margin-bottom: 2%;
    width: 50%;
    margin-left: 25%;
    height: 2px;
    background-color: lightgrey;
  }
  .md-drawer {
    width: 230px;
    max-width: calc(100vw - 125px);
  }
  .md-toolbar-row {
    transition: 0.5s height ease-in-out;
    overflow: hidden;
  }
  #toolbar{
    transition: 0.5s height ease-in-out;
    overflow: hidden;
  }

@media (max-width:991px) {
  .md-content.md-theme-default {
  width: 100%;
  }
  .page-container{
    max-width: 100%;
  }
  #toolbar{
    max-width: 100%;
  }
  .md-resp{
    max-width: 100%;
  }
  .md-toolbar-row{
    max-width: 100%;

  }
   .position{
    position: absolute;
    right: 10px;
    }
}

@media (max-width: 767px) {
  .md-content.md-theme-default {
    width: 100%;
  }
  .page-container{
    max-width: 100%;
  }
  #toolbar{
    max-width: 100%;
  }
  .md-resp{
    max-width: 100%;
  }
  .md-toolbar-row{
    max-width: 100%;

  }
}
</style>
