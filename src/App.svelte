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
      <Route path="/html" component={Html}/>
      <Route path="/css" component={Css}/>
      <Route path="/javascript" component={JavaScript}/>
      <Route path="/node-js" component={Nodejs}/>
      <Route path="/docker" component={Docker}/>
      <Route path="/react" component={React}/>
      <Route path="/svelte" component={Svelte}/>
  </Router>
</main>

<style>
</style>
