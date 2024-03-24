<script>
  import docker from "../../assets/logo-docker.svg";
  import react from "../../assets/react.svg";
  import css from "../../assets/css.svg";
  import node from "../../assets/node.svg";
  import svelte from "../../assets/svelte.svg";
  import { onMount } from "svelte";

  //TODO: Formas de capturar un elemento en svelte y realizar su evento sin errores

  //TODO: primera

  /* onMount nos permite realizar la captura como vanilla JS
  por ejemplo const valor = document.querySelector('valor') 
  cuando los capturamos los tratamos como si fuera vanilla con los ventos t demas
  */

  //TODO: segundo

 /*  con el evento on:mousemove el cual apra utilizarlo en svelte tenemos que
  colocar una etiqueta de comentario
  <!-- svelte-ignore a11y-no-static-element-interactions -->
  y realizamos una funcion con el parametro e que seria nuestro evento 

  en esta forma podemos guardar los valores en una variable con lo que nos sirva 
  del evento ejemplo clientX o clientY y despues realizar la accion en la pripiedad style 
  en la etiqueta HTML ejemplo : style={translate: ${valor}%} o lo que se necesite hacer 
  */

  //TODO : tercero 

  /* usamos la propiedad de svelte en el elemento bind:this={valor} 
  donde el valor de lo declaramos como u na variable esta variable despues podemos ponerla dentro del onmount 
  y usar el addvenetListener en ella evemplo valor.addEventListener('evento', funcion ) y la funcion
  la desarrollamos afuera del onMount
  */

  const sFront = 150;
  const sLetra = -10;
  const sBack = -150;
  let m = { x: 0, y: 0 };
  let sectionElement;
  let front;
  let letra;
  let back;

   onMount(() => {
/*     const paralax = document.querySelector(".paralax");
    const front = document.querySelector(".front-layer");
    const letra = document.querySelector(".layer-1"); */

    sectionElement.addEventListener('mousemove', paralax2)
   
/*      paralax.addEventListener("mousemove", (Event) => {
       m.x = Event.clientX;
       m.y = Event.clientY;
 
       front.style.transform = `translate(${m.x / sFront}%, ${m.y / sFront}%)`;
 
       letra.style.transform = `translate(${m.x / sLetra}%, ${m.y / sLetra}%)`;
     }); */
  });
/*   const paralaxx = (Event) => {
    m.x = Event.clientX;
    m.y = Event.clientY;
    console.log(m.x, m.y)
  } */

  function paralax2(Event){
    m.x = Event.clientX;
    m.y = Event.clientY;
    front.style.transform = `translate(${m.x / sFront}%, ${m.y / sFront}%)`;
    letra.style.transform = `translate(${m.x / sLetra}%, ${m.y / sLetra}%)`;
    back.style.transform = `translate(${m.x / sBack}%, ${m.y / sBack}%)`;
  }

</script>

<!-- svelte-ignore a11y-no-static-element-interactions -->
<section  class="paralax" bind:this={sectionElement}>
  <h2 class="layer-1" bind:this={letra}>ECOS-OI2</h2>
  <div class="front-layer" bind:this={front} >
    <img src={docker} alt="" class="layer" />
    <img src={react} alt="" class="layer" />
    <img src={css} alt="" class="layer" />
    <img src={node} alt="" class="layer" />
    <img src={svelte} alt="" class="layer" />
  </div>
  <div class="back-layer" bind:this={back} >
    <img src={docker} alt="" class="layer" />
    <img src={react} alt="" class="layer" />
    <img src={css} alt="" class="layer" />
    <img src={node} alt="" class="layer" />
    <img src={svelte} alt="" class="layer" />
  </div>
</section>

<style>
  .paralax {
    position: relative;
    background: linear-gradient(#333, #111);
    width: 100%;
    height: 100vh;
    display: flex;
    overflow: hidden;
  }
  .paralax h2 {
    margin: 0;
    color: #fff;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    text-transform: uppercase;
    font-size: 9em;
    line-height: 1.4em;
    z-index: 3;
  }
  .back-layer,
  .front-layer {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
  }

  .front-layer{
    z-index: 1;
  }

  .back-layer{
    z-index: 0;
  }

  
  .front-layer img {
    position: absolute;
    max-width: 220px;
  }

  .back-layer img{
    position: absolute;
    max-width: 500px;
    opacity: 0.5;
  }

  .front-layer img:nth-child(1) {
    top: 0;
    left: 20%;
    width: 16%;
  }
  .back-layer img:nth-child(1) {
    top: 0;
    left: 20%;
    width: 20%;
  }

  .front-layer img:nth-child(2) {
    top: 50%;
    left: 0;
    width: 13%;
  }

  .back-layer img:nth-child(2) {
    top: 50%;
    left: 0;
    width: 20%;
  }

  .front-layer img:nth-child(3) {
    bottom: 0%;
    left: 30%;
    width: 14%;
  }

  .back-layer img:nth-child(3) {
    bottom: 0%;
    left: 30%;
    width: 20%;
  }

  .front-layer img:nth-child(4) {
    bottom: 20%;
    right: 10%;
    width: 12%;
  }
  .back-layer img:nth-child(4) {
    bottom: 20%;
    right: 10%;
    width: 20%;
  }

  .front-layer img:nth-child(5) {
    top: 10%;
    right: 30%;
    width: 11%;
  }
  .back-layer img:nth-child(5) {
    top: 10%;
    right: 30%;
    width: 20%;
  }
</style>
