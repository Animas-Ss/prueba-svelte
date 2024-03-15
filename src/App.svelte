<script>
  import { Route, Router } from 'svelte-routing'
  import Navegation from "./components/Navegation.svelte";
  import Html from './pages/Html/Html.svelte';
  import Css from './pages/Css/Css.svelte';
  import JavaScript from './pages/JavaScript/JavaScript.svelte';
  import Nodejs from './pages/Nodejs/Nodejs.svelte';
  import Docker from './pages/Docker/Docker.svelte';
  import React from './pages/React/React.svelte';
  import Svelte from './pages/Svelte/Svelte.svelte';
</script>

<main>
  <Router>
      <Route path="/prueba-svelte/" component={Navegation} /> 
      <Route path="/prueba-svelte/documentacion/html" component={Html}/>
      <Route path="/prueba-svelte/documentacion/css" component={Css}/>
      <Route path="/prueba-svelte/documentacion/javascript" component={JavaScript}/>
      <Route path="/prueba-svelte/documentacion/node-js" component={Nodejs}/>
      <Route path="/prueba-svelte/documentacion/docker" component={Docker}/>
      <Route path="/prueba-svelte/documentacion/react" component={React}/>
      <Route path="/prueba-svelte/documentacion/svelte" component={Svelte}/>
  </Router>
</main>

<style>
</style>
