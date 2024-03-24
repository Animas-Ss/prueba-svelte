<script>
  import GoBack from "../../components/GoBack.svelte";
  let w = window.innerWidth;

  window.addEventListener('resize', () =>{
    w = window.innerWidth;
  })
</script>

<section>
    <div class="container">
<!--         {#if w < 1040}
        <button class="btn-menu">menu</button>
        {/if} -->
       <div>1 - logo</div>
       <div>2 - busqueda configuracion navbar</div>
       <div>3 - menu</div>
       <div>4 - contenido</div>
       <div>5 - subtitulos</div>
    </div>
</section>

<style>
    section{
        width: 100%;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .container{
        width: 100%;
        height: 100%;
        background: lightcyan;
        display: grid;
        grid-template-rows: 100px auto;
        grid-template-columns: 250px auto 200px;
        grid-template-areas: 
        "c1 c2 c2"
        "c3 c4 c5"
        "c3 c4 c5"
        "c3 c4 c5";
    }
    .container div:nth-child(1){
        grid-area: c1;
        background: lightskyblue;
    }
    .container div:nth-child(2){
        grid-area: c2;
        background: lightslategrey;
    }
    .container div:nth-child(3){
        grid-area: c3;
        background: lightpink;
    }
    .container div:nth-child(4){
        grid-area: c4;
        background: lightyellow;
    }
    .container div:nth-child(5){
        grid-area: c5;
        background: lime;
    }

    @media (width < 1040px){
        .container{
        width: 100%;
        height: 100%;
        background: lightcyan;
        display: grid;
        grid-template-rows: 80px 40px;
        grid-template-columns: 100px 1fr;
        grid-template-areas: 
        "c1 c2"
        "c5 c5"
        "c4 c4";
    }
    .container div:nth-child(3){
        display: none;
    }
    }
</style>