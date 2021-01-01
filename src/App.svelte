<script>
	import { Route, router } from "tinro";
	import Home from "./pages/Home.svelte";
	import Completos from "./pages/Completos.svelte";
	import SpO2 from "./pages/SpO2.svelte";

	router.useHashNavigation();
</script>

<div class="m-3">
	<h1 class="text-center">
		<a href="/">
			<i class="fas fa-virus text-green-700" />
			evolución
			<i class="fas fa-virus text-green-700" />
		</a>
	</h1>
</div>

<Route path="/">
	<Home />
</Route>
<Route path="/completos">
	<Completos />
</Route>
<Route path="/spo2">
	<SpO2 />
</Route>
