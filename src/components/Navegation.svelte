<script>
  import { Link, link, links } from "svelte-routing";
</script>


  <nav class="container" use:links>
    <div class="container-proyectos">
      <div class="proyecto">
        <Link to="/html">
          HTML
        </Link>
      </div>
      <div class="proyecto">
          <Link to="/css" >
          CSS
        </Link>  
      </div>
      <div class="proyecto">
          <Link to="/javascript">
          JAVASCRIPT
        </Link>
        </div>
        <div class="proyecto">
          <Link to="/node-js">
          NODE.JS
        </Link>
      </div>
      <div class="proyecto">
          <Link to="/docker">
          DOCKER
        </Link>
        </div>
        <a href="/react" class="proyecto">
          REACT
        </a>
        <a href="/svelte" class="proyecto" use:link>
          SVELTE
        </a>
    </div>
  </nav>


<style>
  .container {
    width: 100%;
    height: 100vh;
  }
  .proyecto {
    display: flex;
    align-items: center;
    justify-content: center;
    background: #414141;
    border: 1px solid #ffffff;
    border-radius: 10px;
    font-size: 3rem;
    color: #ffffff;
    transition: all 500ms ease;
  }
  .container-proyectos {
    padding: 20px;
    width: 100%;
    height: 100vh;
    background: #313131;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 10px;
    overflow: hidden;
  }

  /*.proyecto:nth-child(1){
    grid-column: span 2;
    grid-row: span 1;}*/

  .proyecto:nth-child(7n + 1) {
    grid-column: span 2;
    grid-row: span 1;
  }

  /*   .proyecto:nth-child(2) {
    grid-column: span 1;
    grid-row: span 2;
  }
 */

  .proyecto:nth-child(7n + 2) {
    grid-column: span 1;
    grid-row: span 2;
  }
  /*   .proyecto:nth-child(3) {
    grid-column: span 1;
    grid-row: span 2;
  } */

  .proyecto:nth-child(7n + 4) {
    grid-column: span 1;
    grid-row: span 2;
  }

  .proyecto:nth-child(7n + 7) {
    grid-column: span 3;
    grid-row: span 1;
  }

  .proyecto:hover {
    z-index: 100;
    transform: scale(1.1);
    box-shadow: 20px 20px 30px rgba(0, 0, 0, 1);
  }
</style>
