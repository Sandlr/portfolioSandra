<template>
  <div>
    <div class="container22">
      <h1 class="me"></h1>
      <div id="animate22" class="roll22">
        <img id="reveal22" class="im" src="img/pic.png" />
      </div>
      <div class="exposicion22">
        <div class="tit">
          <b>ABOUT ME</b>
        </div>
        <br />

        Soy Sandra López estudiante de tercer curso de Diseño gráfico en la
        Escuela Superior de Diseño de Madrid. Además de ello, también me
        encuentro en mi último año de la carrera Publicidad y Relaciones
        Públicas en la Universidad Complutense.
        <br />
        <br />
        En cuanto a mis capacidades he de destacar que me considero una persona
        responsable y trabajadora, con facilidad para aprender y desarrollar
        tareas grupales.
        <br />
        <br />
        A cerca de las principales herramientas que manejo, he de resaltar el
        paquete completo de Adobe, Procreate y Cinema 4D.
        <br />
        <br />
        Contacto: slopez3030@esdmadrid.es
      </div>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    const controller = new this.$scrollmagic.Controller();

    var scene22 = new this.$scrollmagic.Scene({
      triggerElement: ".container22",
      duration: 1000,
      triggerHook: 0.5, // show, when scrolled 10% into view
      duration: "100%", // hide 10% before exiting view (80% + 10% from bottom)
      offset: 50,
    })
      .setTween(".me", 0.5, { scale: 0.8 })
      .setClassToggle("#reveal22", "visible") // add class to reveal
      .addTo(controller);
  },
};
</script>

<style lang="scss">
/* {
  border: 1px solid pink;
}*/
.container22 {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  
  padding-bottom: 1rem;
  flex-direction: row;
  .roll22 {
    display: flex;
    justify-content: space-evenly;
    .im {
      width: 160px;
    }
  }
}
#reveal22 {
  opacity: 0;
  -webkit-transform: scale(0.9);
  -moz-transform: scale(0.9);
  -ms-transform: scale(0.9);
  -o-transform: scale(0.9);
  transform: scale(0.9);
  -webkit-transition: all 350ms ease-in-out;
  -moz-transition: all 350ms ease-in-out;
  -ms-transition: all 350ms ease-in-out;
  -o-transition: all 350ms ease-in-out;
  transition: all 350ms ease-in-out;
}
#reveal22.visible {
  opacity: 1;
  -webkit-transform: none;
  -moz-transform: none;
  -ms-transform: none;
  -o-transform: none;
  transform: none;
}

.exposicion22 {
  width: 700px;
  display: flex;
  flex-direction: column;
  text-align: left;
  padding-left: 4rem;
  margin-top: 0rem;

  .tit {
    color: #fe6f35;
  }
}

@media screen and (max-width: 600px) {

.container22 {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  
  padding-bottom: 1rem;
  flex-direction: column;
  .roll22 {
    display: flex;
    justify-content: space-evenly;
    .im {
      width: 150px;
      
    }
  }
}


.exposicion22 {
  width: 320px;
  display: flex;
  flex-direction: column;
  text-align: left;
  padding-left: 1rem;
  margin-top: 4rem;
  font-size: 12px;

  .tit {
    color: #fe6f35;
  }
}


}
</style>
