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
      <Route path="/" component={Navegation} /> 
      <Route path="/documentacion/html" component={Html}/>
      <Route path="/documentacion/css" component={Css}/>
      <Route path="/documentacion/javascript" component={JavaScript}/>
      <Route path="/documentacion/node-js" component={Nodejs}/>
      <Route path="/documentacion/docker" component={Docker}/>
      <Route path="/documentacion/react" component={React}/>
      <Route path="/documentacion/svelte" component={Svelte}/>
  </Router>
</main>

<style>
</style>
