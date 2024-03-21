<script>
  import { links } from "svelte-routing";
  import html from "../assets/html.svg";
  import javascript from '../assets/javascript-logo.svg';
  import css from '../assets/css.svg';
  import nodeJs from '../assets/node.svg';
  import docker from '../assets/logo-docker.svg';
  import react from '../assets/react.svg';
  import svelte from '../assets/svelte.svg';
</script>

<nav class="container" use:links>
  <div class="container-proyectos">
    <a href="/html" class="proyecto">
      <img src={html} class="icono" alt="icon html" />
    </a>
    <a href="/css" class="proyecto">
      <img src={css} class="icono" alt="icon html" />
    </a>
    <a href="/javascript" class="proyecto">
      <img src={javascript} class="icono" alt="icon javascript" />
    </a>
    <a href="/node-js" class="proyecto">
      <img src={nodeJs} class="icono" alt="icon nodejs" />
    </a>
    <a href="/docker" class="proyecto">
      <img src={docker} class="icono" alt="icon docker" />
    </a>
    <a href="/react" class="proyecto">
      <img src={react} class="icono" alt="icon react" />
    </a>
    <a href="/svelte" class="proyecto">
      <img src={svelte} class="icono" alt="icon svelte" />
    </a>
  </div>
</nav>

<style>
  .container {
    width: 100%;
    height: 100vh;
    font-family: "Roboto", sans-serif;
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
    text-decoration: none;
  }
  .icono {
    width: 40px;
    height: 40px;
  }
  .container-proyectos {
    padding: 60px;
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
  
  @media (width < 1040px){
    .container-proyectos{
      padding: 10px;
      grid: grid;
      grid-template-columns: repeat(2, 1fr);
      grid-template-rows: repeat(7, 100px);
      overflow: auto;
    }
    .proyecto:nth-child(7n + 1) {
    grid-column: span 1;
    grid-row: span 1;
  }
  .proyecto:nth-child(7n + 2) {
    grid-column: span 1;
    grid-row: span 2;
  }
  .proyecto:nth-child(7n + 4) {
    grid-column: span 2;
    grid-row: span 1;
  }

  .proyecto:nth-child(7n + 7) {
    grid-column: span 2;
    grid-row: span 1;
  }
  }
  
</style>
