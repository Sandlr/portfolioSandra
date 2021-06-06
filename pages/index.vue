<template>
  <div>
    <div class="container">
      <div class="texto_principal">
        <h1 class="title">¡Hola!</h1>
        <div class="subtitle">
          Mi nombre es Sandra López, soy estudiante de Diseño gráfico <br />
          además de Publicidad y Relaciones Públicas
        </div>
        <br />

        <div class="base">
          De manera generaliza, me es de gran interés todo aquello que tenga que
          ver con el panorama audiovisual. No obstante, a lo largo de mis
          estudios he sentido una gran predilección por aquellos proyectos
          relacionados con la dirección de arte y su posterior aplicación.
        </div>
      </div>
    </div>
    <div class="container3">
      <div class="texto_miniproject">
        <h1 class="title_miniproject">Knolling</h1>

        <br />

        <div class="base_miniproject">
          Nos encontramos ante un encargo de fotografía deconstructiva, la idea
          radica en plasmar mediante esta técnica nuevas recetas que puedan
          plasmarse en la carta de un restaurante toscano. Todo ello mediante
          composiciones sencillas, versátiles y cohesionadas.
        </div>
      </div>
    </div>

    <div class="container2">
      <h1 class="knol"></h1>
      <div id="animate2" class="roll">
        <img
          id="reveal2"
          class="comida1"
          src="img/pasta.jpg"
          alt="mukumbari"
        />
        <img
          id="reveal2"
          class="comida2"
          src="img/ensalada.jpg"
          alt="lobatera"
        />
        <img
          id="reveal2"
          class="comida3"
          src="img/postre.jpg"
          alt="observatorio"
        />
      </div>
    </div>

    <div class="container4">
      <div class="texto_miniproject4">
        <h1 class="title_miniproject4">Primavera</h1>

        <br />

        <div class="base_miniproject4">
          Retrato de aire primaveral y fresco, iluminado con flash de mano.
          <br />
          <br />
          Modelo: Celia Roncero
        </div>
      </div>
    </div>

    <div class="container5">
      <h1 class="knol5"></h1>
      <div id="animate5" class="roll5">
        <img
          id="reveal5"
          class="comida5"
          src="img/celia1.jpg"
          
        />
        <img
          id="reveal5"
          class="comida6"
          src="img/celia2.jpg"
          
        />
        <img
          id="reveal5"
          class="comida7"
          src="img/celia3.jpg"
          
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    const controller = new this.$scrollmagic.Controller();

    var scene3 = new this.$scrollmagic.Scene({
      triggerElement: ".container2",
      duration: 1000,
      triggerHook: 0.5, // show, when scrolled 10% into view
      duration: "100%", // hide 10% before exiting view (80% + 10% from bottom)
      offset: 50,
    })
      .setTween(".knol", 0.5, { scale: 0.8 })
      .setClassToggle("#reveal2", "visible") // add class to reveal
      .addTo(controller);

    var scene5 = new this.$scrollmagic.Scene({
      triggerElement: ".container5",
      duration: 1000,
      triggerHook: 0.5, // show, when scrolled 10% into view
      duration: "100%", // hide 10% before exiting view (80% + 10% from bottom)
      offset: 50,
    })
      .setTween(".knol5", 0.5, { scale: 0.8 })
      .setClassToggle("#reveal5", "visible") // add class to reveal
      .addTo(controller);
  },
};
</script>

<style lang="scss">

/* {
  border: 1px solid pink;
}*/

.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  padding-left: 5rem;
  align-items: center;
}
.texto_principal {
  display: flex;
  justify-content: left;
  flex-direction: column;
  margin-top: 200px;
}

.title {
  font-family: Roboto, "Helvetica Neue", Arial, sans-serif;

  font-size: 62px;
  color: #a60e00;
  letter-spacing: 1px;
  font-weight: bold;
}

.subtitle {
  font-family: Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 22px;
  color: #526488;
  margin-top: 20px;
  width: 700px;
  display: flex;
}

.base {
  font-family: Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 14px;
  width: 620px;
}

//Knolling
.container3 {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  padding-left: 5rem;
  align-items: center;
  background-color: rgb(196, 231, 253);
  justify-content: flex-end;
  padding-right: 12rem;
}
.texto_miniproject {
  display: flex;
  justify-content: right;
  flex-direction: column;
  margin-top: 200px;
  color: black;
}

.title_miniproject {
  font-family: Roboto, "Helvetica Neue", Arial, sans-serif;

  font-size: 62px;
  color: #a60e00;
  letter-spacing: 1px;
  font-weight: bold;
}

.base_miniproject {
  font-family: Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 14px;
  width: 620px;
  color: black;
}

.container2 {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background: #ffffff;
  padding-bottom: 1rem;
  .roll {
    display: flex;
    justify-content: space-evenly;
    .comida1 {
      margin: 0rem;
      height: 20%;
      width: 20%;
    }
    .comida2 {
      margin-top: 5rem;
      height: 20%;
      width: 20%;
    }
    .comida3 {
      margin-top: 10rem;
      height: 20%;
      width: 20%;
    }
  }
}

#reveal2 {
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
#reveal2.visible {
  opacity: 1;
  -webkit-transform: none;
  -moz-transform: none;
  -ms-transform: none;
  -o-transform: none;
  transform: none;
}
//Primavera
.container4 {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  padding-left: 5rem;
  align-items: center;
  background-color: #fe6f35;
  justify-content: flex-end;
  padding-right: 12rem;
}
.texto_miniproject4 {
  display: flex;
  justify-content: right;
  flex-direction: column;
  margin-top: 200px;
  color: #ffffff;
}

.title_miniproject4 {
  font-family: Roboto, "Helvetica Neue", Arial, sans-serif;

  font-size: 62px;
  color: #ffffff;
  letter-spacing: 1px;
  font-weight: bold;
}

.base_miniproject4 {
  font-family: Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 14px;
  width: 620px;
  color: #ffffff;
}
.links {
  padding-top: 15px;
}

.container5 {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  background: #ffffff;
  padding-bottom: 1rem;
  .roll5 {
    display: flex;
    justify-content: space-evenly;
    .comida5 {
      margin-top: 10rem;
      height: 30%;
      width: 30%;
    }
    .comida6 {
      margin-top: 5rem;
      height: 30%;
      width: 30%;
    }
    .comida7 {
      margin-top: 0rem;
      height: 30%;
      width: 30%;
    }
  }
}

#reveal5 {
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
#reveal5.visible {
  opacity: 1;
  -webkit-transform: none;
  -moz-transform: none;
  -ms-transform: none;
  -o-transform: none;
  transform: none;
}
</style>
