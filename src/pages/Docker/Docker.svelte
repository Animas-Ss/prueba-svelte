<script>
  import GoBack from "../../components/GoBack.svelte";
  let menuShadow = false;
  let w = window.innerWidth;
  window.addEventListener('resize', () => {
    w = window.innerWidth
  })

  const handleShadow = () => {
    menuShadow = !menuShadow;
  }
</script>

<section>
    <div class="contenido">
<!--         <div class="titulos">
            <GoBack/>
            <h1>Docker documentacion</h1>
        </div> -->
        <div class="container">
            {#if w < 600}
            <button class="bt-menu" on:click={handleShadow}>menu</button>
            {/if}
            <div class={menuShadow ? "activo" : "barra-lateral"}>
                <div>
  
                </div>
            </div>
            <div class="apuntes">
                <div>2</div>
                <div>3</div>
                <div>4</div>
            </div>
        </div>
    </div>
</section>

<style>
/*     section{
        position: relative;
        width: 100%;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        z-index: 1;
        background: #1B1B1F;
        overflow: hidden;
    }
    section::before{
        content: '';
        position: absolute;
        display: block;
        top: 0;
        right: 0px;
        width: 600px;
        height: 600px;
        background: url(../../assets/logo-docker.svg) no-repeat;
        background-size: contain;
        filter: drop-shadow(10px 10px 15px rgba(0, 0, 0, 0.6));
        z-index: 2;
    }
    .contenido{
        position: absolute;
        z-index: 5;
        width: 100%;
        height: 100%;
        display: grid;
        grid-template-columns: repeat(auto-fit,minmax(150px, 1fr));
        padding: 30px;
        gap: 20px;
    }
    .titulos{
        grid-column: 1/3;
        grid-row: auto;
        background: rgba(255, 255, 255, 0.4);
    }
    div:nth-child(2){
        grid-column: 3 / 13;
        grid-row: auto;
    } */
   /*  probamos grind */
   .container{
      background: salmon;
      border: 2px solid black;
      border-radius: 10px;
      height: 100vh;
      display: grid;
      grid-template-columns: minmax(100px, 200px) 1fr;
      grid-gap: 5px;
   }
   .container div{
    background: lightblue;
    border: 1px solid #09f;
   }
   .apuntes{
    display: grid;
    grid-template-columns: 1fr 200px;
    grid-template-rows: 80px 1fr;
   }
   .apuntes div:nth-child(3n +1){
      grid-column: span 2;
   }
   .apuntes div:nth-child(3n +2){
      background: red;
   }
   .apuntes div:nth-child(3n +3){
     background: blueviolet;
   }

   @media (width < 1000px){
    .apuntes{
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 80px 70px 1fr ;
   }
   .apuntes div:nth-child(3n +3){
     background: blueviolet;
     grid-column: span 2;
     grid-row: 2 / 3;
   }
   }

   @media (width < 600px){
    .container{
        grid-template-columns: 1fr;
    }
    .barra-lateral{
    display: none
   }
    .activo{
    display: grid;
    position: absolute;
    width: 200px;
    height: 100%;
    background: black;
    }
   .bt-menu{
    position: absolute;
    width: 40px;
    height: 40px;
    z-index: 4;
   }
   .apuntes div:nth-child(3n +3){
     background: blueviolet;
     grid-column: span 2;
     grid-row: 2 / 3;
   }
   }
</style>