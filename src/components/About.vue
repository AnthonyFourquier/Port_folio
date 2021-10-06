<template>
  <div id="about">
    <div id="about-container">
      <md-field>
        <label >Nom</label>
        <md-input v-model="lastname"></md-input>
      </md-field>

      <md-field>
        <label>Prénom</label>
        <md-input v-model="firstname"></md-input>
      </md-field>

      <md-field>
        <label>Mail</label>
        <md-input v-model="mail" type="mail"></md-input>
      </md-field>

      <md-field>
        <label>Objet</label>
        <md-input v-model="object"></md-input>
      </md-field>

      <md-field >
        <label >Expliquer en quelques mots ...</label>
        <md-textarea v-model="textarea" ></md-textarea>
      </md-field>
    </div>
    <div style="height:1px"></div>
  </div>
</template>

<script>
export default {
  name: "TextFields",
  data: () => ({
    lastname: null,
    firstname: null,
    mail: null,
    textarea: null,
    object: null,
  }),
};
</script>
<style scoped>
#about{
display: none;
}
.md-field.md-theme-default:before{
  background-color: #00314c;
}

.md-field.md-theme-default.md-focused label{
  color: #00314c; 
}

#about-container {
  margin-bottom: 5%;
  width: 50%;
  margin-left: 25%;
  border: 1px solid white;
  box-shadow: 0px 4px 24px rgba(0, 0, 0, 0.2);
  padding: 10px;
  background-color: white;
}

#about {
  margin-top: 120px;

}
@media screen and (max-width: 500px) {
  #about{
    margin-left: 10%;
    margin-top: 75px;
    }
  #about-container  {
    width: 90%;
    margin-left: 0;

    }
  }
@media screen and (min-width: 501px) and (max-width: 1024px) {
    #about{
    margin-left: 10%;
    margin-top: 75px;
    }
  #about-container  {
    width: 90%;
    margin-left: 0;
    }
}
</style>
