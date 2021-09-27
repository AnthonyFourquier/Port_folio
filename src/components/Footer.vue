<template>
  <div id="footer">
    <div style="height:5px"></div>
    <button><a
                    id="link"
                    href="https://www.linkedin.com/in/anthony-fourquier"
                    target="_blank"
                  ><i class="fab fa-linkedin-in "></i></a></button>
    <button><a
                    id="link"
                    href="https://www.github.com/AnthonyFourquier"
                    target="_blank">
                   <i class="fab fa-github"></i></a></button>
    <button><i class="fab fa-instagram"></i></button>
    <button><a id="link" href="mailto:fourquier.anthony@hotmail.fr"><i class="fas fa-at"></i></a></button>
    <button><a id="link" href="tel:+0627575561"><i class="fas fa-phone"></i></a></button>
   <div style="height:5px"></div>
  </div>
</template>

<script>
export default {
  name: "Footer",

};
</script>
<style scoped>
#footer{
position: fixed;
width: 54px;
height: 250px;
right: 4vh;
bottom: 10vh;


background: rgba(0, 0, 0, 0.24);
border-radius: 27px;
display: flex;
flex-direction: column;
justify-content: space-around;
z-index: 2;
}
button{
background: rgba(23, 23, 23, 0.5);
border: 1px solid rgba(255, 255, 255, 0.5);
box-sizing: border-box;
color: white;
border-radius: 75px;
width: 38px;
height: 38px;
margin: auto;
}
i{
  margin: auto;
}
#link {
  text-decoration: none;
  color: white;
}

@media screen and (max-width: 500px) {
  #footer{
    max-width: 90%;
    margin: auto;
    top: 50px;
    right: 15px;
  }
}
@media screen and (min-width: 501px) and (max-width: 1024px) {
   #footer{
    margin: auto;
    max-width: 90%;
    top: 120px;
    right: 10px;
  }
}
</style>
