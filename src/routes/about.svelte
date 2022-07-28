<script context="module">
	import { browser, dev } from '$app/env';

	// we don't need any JS on this page, though we'll load
	// it in dev so that we get hot module replacement...
	export const hydrate = dev;

	// ...but if the client-side router is already loaded
	// (i.e. we came here from elsewhere in the app), use it
	export const router = browser;

	// since there's no dynamic data here, we can prerender
	// it so that it gets served as a static asset in prod
	export const prerender = true;
</script>

<svelte:head>
	<title>About</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="content">
	<h1>About this site</h1>
	
	<h2>Who am I</h2>

	<p>
		My name is <a href="https://twitter.com/KedziorArtur">Artur Kedzior</a> and I'm a software engineer based in Spain. 
		I created this site to help people make their own <strong>solar pool heaters</strong> just as I did with my pool.
	</p>

	<h2>But why?</h2>

	<p>
		My pool is in the mountain house at 995m (XXXft) above the sea level in the province of Alicante, Spain. 
		Although it's hot in here during the summer, the pool temperature usually stays between 25-27C (x-x F) which is <strong>freaking cold</strong>! 
	</p>

	<h2>What did I do?</h2>

	<p>
		I have watched all the videos of this amazing dude (<a href="https://www.youtube.com/user/gabrielgroso/videos">SolarHeatOK</a>) which shared all his findings through experimenting and I thought it will be fun to put this all together. 
	</p>
</div>

<style>
	.content {
		width: 100%;
		max-width: var(--column-width);
		margin: var(--column-margin-top) auto 0 auto;
	}
</style>
