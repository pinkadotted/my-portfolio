<script>
	// The ordering of these imports is critical to your app working properly
	import '@skeletonlabs/skeleton/themes/theme-modern.css';
	// If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
	import '@skeletonlabs/skeleton/styles/all.css';
	// Most of your app wide CSS should be put in this file
	import '../app.postcss';

	import { AppShell, AppBar, LightSwitch } from '@skeletonlabs/skeleton';

	function scrollIntoView({ target }) {
		  const el = document.querySelector(target.getAttribute('href'));
		  if (!el) return;
	  el.scrollIntoView({
		behavior: 'smooth'
	  });
	}

	const downloadResume = () => {
		return;
	}
</script>

<!-- <slot /> -->

<AppShell>
	<svelte:fragment slot="header">
	
		
	<AppBar>
		<svelte:fragment slot="lead">
			<div class="placeholder-circle w-16 animate-pulse" />
		</svelte:fragment>
		Subesh's portfolio
		<svelte:fragment slot="trail">
			
		<a href="#about" class="btn variant-ghost-primary" on:click|preventDefault={scrollIntoView}>
			<span>About</span>
		</a>

		<a href="#past-projects" class="btn variant-ghost-primary" on:click|preventDefault={scrollIntoView}>
			<span>Past Projects</span>
		</a>
		<a href="#skills" class="btn variant-ghost-primary" on:click|preventDefault={scrollIntoView}>
			<span>Skills</span>
		</a>
		<a href="#contact" class="btn variant-ghost-primary" on:click|preventDefault={scrollIntoView}>
			<span>Contact</span>
		</a>

		<a href="#download-resume" class="btn variant-ghost-primary" on:click|preventDefault={downloadResume}>
			<span>Download Resume</span>
		</a>

	<LightSwitch />
		</svelte:fragment>
	</AppBar>

	</svelte:fragment>
	<!-- Router Slot -->
	<slot />

	<!-- ---- / ---- -->

	<!-- <svelte:fragment slot="pageFooter">Page Footer</svelte:fragment> -->
</AppShell>