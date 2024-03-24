<script>
  import GoBack from "../../components/GoBack.svelte";
</script>

<section>
  <div class="circulo"></div>
</section>

<style>
  section {
    width: 100%;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background: #e7caca;
    overflow: hidden;
  }
  .circulo {
    position: relative;
    width: 300px;
    height: 300px;
    display: flex;
    justify-content: center;
    align-items: center;
    background: transparent;
    border-radius: 50%;
    border: 2px solid #e7caca;
    transition: all 4s ease-in-out;
    box-shadow:
      -3px -3px 7px rgba(255, 255, 255, 1),
      3px 3px 5px rgba(168, 146, 146, 0.7);
    animation: gota 4s linear infinite;
    animation-delay: 1s;
  }

  .circulo::before {
    content: "";
    position: absolute;
    width: 200px;
    height: 200px;
    background: transparent;
    border-radius: 50%;
    border: 2px solid #e7caca;
    transition: all 2s ease-in-out;
    box-shadow:
      -3px -3px 7px rgba(255, 255, 255, 1),
      3px 3px 5px rgba(168, 146, 146, 0.7);
    animation: gota 4s linear infinite;
    z-index: 3;
  }
  .circulo::after {
    content: "";
    position: absolute;
    width: 400px;
    height: 400px;
    background: transparent;
    border-radius: 50%;
    border: 4px solid #e7caca;
    transition: all 2s ease-in-out;
    box-shadow:
      -3px -3px 7px rgba(255, 255, 255, 1),
      3px 3px 5px rgba(168, 146, 146, 0.7);
    animation: gota 4s linear infinite;
    animation-delay: 2s;
  }

  @keyframes gota {
    0% {     
        box-shadow:
        -4px -4px 8px rgba(255, 255, 255, 1),
        4px 4px 7px rgba(168, 146, 146, 0.7);
        opacity: 1;
      }

    50% {
      box-shadow:
        -2px -2px 4px rgba(255, 255, 255, 1),
        2px 2px 3px rgba(168, 146, 146, 0.7);
        opacity: 0.5;
    }
    100% {
      box-shadow:
        0pc 0px 0px rgba(255, 255, 255, 1),
        0px 0px 0px rgba(168, 146, 146, 0.7);
        opacity: 0;
    }
  }
</style>
