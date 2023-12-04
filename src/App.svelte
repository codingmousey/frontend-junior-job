<script>
	import { Router, Route } from 'svelte-routing';
	import Header from './Header.svelte';
	import Main from './Main.svelte';
	import Signup from './Signup.svelte';
  
	let sitename = "Junior Job";
  </script>
  
  <div>
	<Header {sitename} />
  
	<Router>
	  <Route path="/" component={Main} />
	  <Route path="/signup" component={Signup} />
	</Router>
  </div>

<style>
</style>