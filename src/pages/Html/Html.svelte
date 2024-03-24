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
        3px 3px 5px rgba(168, 146, 146, 0.7),
        inset -3px -3px 7px rgba(255, 255, 255, 1),
        inset 3px 3px 5px rgba(168, 146, 146, 0.7);
      animation: gota 4s linear infinite;
      animation-delay: 5s;
      opacity: 0;
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
        3px 3px 5px rgba(168, 146, 146, 0.7),
        inset -3px -3px 7px rgba(255, 255, 255, 1),
        inset 3px 3px 5px rgba(168, 146, 146, 0.7);
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
        3px 3px 5px rgba(168, 146, 146, 0.7),
        inset -3px -3px 7px rgba(255, 255, 255, 1),
        inset 3px 3px 5px rgba(168, 146, 146, 0.7);
      animation: gota 4s linear infinite;
      animation-delay: 6s;
      opacity: 0;
    }
  
    @keyframes gota {
      0% {
        box-shadow:
          -3px -3px 7px rgba(255, 255, 255, 1),
          3px 3px 5px rgba(168, 146, 146, 0.7),
          inset -3px -3px 7px rgba(255, 255, 255, 1),
          inset 3px 3px 5px rgba(168, 146, 146, 0.7);
          transform: rotate(0);
          transform: scale(0.5);
          opacity: 0;
      }
      50% {
        box-shadow:
          -1px -1px 3px rgba(255, 255, 255, 1),
          1px 1px 2px rgba(168, 146, 146, 0.7),
          inset -1px -1px 3px rgba(255, 255, 255, 1),
          inset 1px 1px 2px rgba(168, 146, 146, 0.7);
          transform: rotate(45);
          transform: scale(1);
          opacity: 1;
      }
      100% {
        box-shadow:
          0pc 0px 0px rgba(255, 255, 255, 1),
          0px 0px 0px rgba(168, 146, 146, 0.7),
          0px 0px 0px rgba(255, 255, 255, 1),
          0px 0px 0px rgba(168, 146, 146, 0.7);
          transform: rotate(360);
          transform: scale(1.2);
          opacity: 0;
      }
    }
  </style>
  