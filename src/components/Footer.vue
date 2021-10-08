<template>
  <div id="footer">
    <div style="height:5px"></div>
    <a
                    id="link"
                    href="https://www.linkedin.com/in/anthony-fourquier"
                    target="_blank"
                  ><button id="btnlinkedin"><i class="fab fa-linkedin-in "></i></button></a>
    <a
                    id="link"
                    href="https://www.github.com/AnthonyFourquier"
                    target="_blank">
                  <button id="btngithub"> <i class="fab fa-github"></i></button></a>
   <!--  <button><i class="fab fa-instagram"></i></button> -->
    <a id="link" href="mailto:fourquier.anthony@hotmail.fr"><button id="btnmail"><i class="fas fa-at"></i></button></a>
    <a id="link" href="tel:+0627575561"><button id="btnphone"><i class="fas fa-phone"></i></button></a>
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
height: 200px;
right: 4vh;
bottom: 10vh;
background: rgba(0, 0, 0, 0.24);
border-radius: 27px;
display: flex;
flex-direction: column;
justify-content: space-around;
z-index: 2;
transition: all 0.5s;
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
transition: all 0.5s;
cursor: pointer;
}
a{
  margin: auto;
}
i{
  margin: auto;
}
#link {
  text-decoration: none;
  color: white;
}
#footer:hover{
  transform: scale(1.5);
  transition-duration: 1s;
  transition-timing-function: cubic-bezier(0.4, 0.0, 0.2, 1);  
}
button:hover{
    transform: scale(1.25);
  transition-duration: 0.5s;
  transition-timing-function: cubic-bezier(0.4, 0.0, 0.2, 1);  
}
#btngithub:hover:after{
  content: "Github";
  position: absolute;
  right: 120%;
  background:rgba(23, 23, 23, 0.5);
  padding: 5px;
  border-radius: 3px;
}
#btnlinkedin:hover:after{
  content: "Linkedin";
  position: absolute;
  right: 120%;
  background:rgba(23, 23, 23, 0.5);
  padding: 5px;
  border-radius: 3px;
}
#btnmail:hover:after{
  content: "Mail";
  position: absolute;
  right: 120%;
  background:rgba(23, 23, 23, 0.5);
  padding: 5px;
  border-radius: 3px;
}
#btnphone:hover:after{
  content: "Téléphone";
  position: absolute;
  right: 120%;
  background:rgba(23, 23, 23, 0.5);
  padding: 5px;
  border-radius: 3px;
}

@media  (max-width: 991px) {
   #footer{
    margin: auto;
    max-width: 90%;
    top: 120px;
    right: 10px;
  }
}
@media (max-width: 767px) {
  #footer{
    display: none;
    max-width: 90%;
    margin: auto;
    top: 50px;
    right: 15px;
  }
}
</style>
