<script lang="ts">
	import '../app.css';
	import Main from '../components/Main.svelte';
	import Landing from '../components/Landing.svelte';
	import Footer from '../components/Footer.svelte';
	let { children } = $props();
</script>

<div
	class="relative flex flex-col max-w-screen mx-auto w-full text-sm
sm: text-base min-h-screen"
>
	<Landing />
	<Main />
	<Footer />
</div>
{@render children()}
