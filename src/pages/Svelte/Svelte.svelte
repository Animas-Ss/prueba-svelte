<script>
    import { onMount } from 'svelte'

  const data = [
    {
      image: "./Firefly.webp",
      name: "Fire Fly",
      description:
        "imagen sacada de internet para prueba de estilo con css estamos usando svelte pero tratandod e respetar el js clasico",
    },
    {
      image: "./sound.jpg",
      name: "Sound",
      description:
        "imagen sacada de internet para prueba de estilo con css estamos usando svelte pero tratandod e respetar el js clasico",
    },
    {
      image: "./podcast.webp",
      name: "PodCast",
      description:
        "imagen sacada de internet para prueba de estilo con css estamos usando svelte pero tratandod e respetar el js clasico",
    },
    {
      image: "./retrato.jpg",
      name: "Retrato",
      description:
        "imagen sacada de internet para prueba de estilo con css estamos usando svelte pero tratandod e respetar el js clasico",
    },
    {
      image: "./retrato.jpg",
      name: "Retrato",
      description:
        "imagen sacada de internet para prueba de estilo con css estamos usando svelte pero tratandod e respetar el js clasico",
    },
    {
      image: "./retrato.jpg",
      name: "Retrato",
      description:
        "imagen sacada de internet para prueba de estilo con css estamos usando svelte pero tratandod e respetar el js clasico",
    },
  ];
  

  onMount(() => {
    const next = document.querySelector('.next');
    const prev = document.querySelector('.prev');

    next.addEventListener('click', () => {
        const items = document.querySelectorAll('.item')
        document.querySelector('.slide').appendChild(items[0])
    })

    prev.addEventListener('click', () => {
        const items = document.querySelectorAll('.item')
        document.querySelector('.slide').prepend(items[items.length -1])
    })

  })

</script>

<section>
  <div class="container">

    <div class="slide">

      {#each data as item}
        <div class="item"  style={`background-image: url(${item.image})`}>
          <div class="content">
            <div class="name">{item.name}</div>
            <div class="des">{item.description}</div>
            <button>More</button>
          </div>
        </div>
      {/each}

    </div>

    <div class="button">
        <button class="next">A</button>
        <button class="prev">T</button>
    </div>

  </div>
</section>

<style>
  section {
    width: 100%;
    height: 100vh;
    background: #eaeaea;
    overflow: hidden;
  }
  .container{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 100%;
    height: 100%;
    background: #f5f5f5;
    box-shadow: 0 30px 50px #dbdbdb;
  }

  .container .slide .item{
    width: 200px;
    height: 300px;
    position: absolute;
    top: 50%;
    transform: translate(0, -50%);
    border-radius: 20px;
    box-shadow: 0 30px 50px #505050;
    background-position: 50% 50%;
    background-size: cover;
    display: inline-block;
    transition:  0.5s;
  }

  .slide .item:nth-child(1),
  .slide .item:nth-child(2){
    top: 0;
    left: 0;
    transform: translate(0, 0);
    border-radius: 0;
    width: 100%;
    height: 100%;
  }

  .slide .item:nth-child(3){
    left: 50%;
  }
  .slide .item:nth-child(4){
    left: calc(50% + 220px);
  }
  .slide .item:nth-child(5){
    left: calc(50% + 440px);
  }
  /** here n= 0,1,2,3,4,...*/
  .slide .item:nth-child(n + 6){
    left: calc(50% + 660px);
    opacity: 0;
    display: none; /* TODO: fundamental apra evitar un error en el css da un salto */
  }

  .item .content{
    position: absolute;
    top: 50%;
    left: 100px;
    width: 300px;
    text-align: left;
    color: #eee;
    transform: translate(0, -50%);
    font-size: system-ui;
    display: none;
  }

  .slide .item:nth-child(2) .content{
    display: block;
  }
   /** generamos una animacion*/
  .content .name{
    font-size: 40px;
    text-transform: uppercase;
    font-weight: bold;
    opacity: 0;
    animation: animate 1s ease-in-out 1 forwards;
  }

  .content .des{
    margin-top: 10px;
    margin-bottom: 20px;
    opacity: 0;
    animation: animate 1s ease-in-out 1 forwards;
  }

  .content button{
    padding: 10px 20px;
    border: none;
    cursor: pointer;
    opacity: 0;
    animation: animate 1s ease-in-out 1 forwards;
  }

  .button{
    width: 100%;
    position: absolute;
    text-align: center;
    bottom: 20px;
  }

  .button button{
    width: 40px;
    height: 35px;
    border-radius: 8px;
    border: none;
    cursor: pointer;
    margin: 0 5px;
    border: 1px solid #000;
    transition: 0.3s;
  }

  .button button:hover{
    background: #ababab;
    color: #fff;
  }


 @keyframes animate{
    from{
        opacity: 0;
        transform: translate(0, 100px);
        filter: blur(33px);
    }
    to{
        opacity: 1;
        transform: translate(0);
        filter: blur(0);
    }
 }
</style>
