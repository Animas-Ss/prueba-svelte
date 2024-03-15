<script>
  import { link } from "svelte-routing";
</script>

<div use:link>
    <a href="/prueba-svelte/">Go Back</a>
</div>

<style>
    div, a{
        width: 60px;
        height: 60px;
        border-radius: 50%;
        text-decoration: none;
        background: blue;
        display: flex;
        justify-content: center;
        align-items: center;
        color: beige;
    }
</style>