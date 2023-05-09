<script>
	// The ordering of these imports is critical to your app working properly
	import '@skeletonlabs/skeleton/themes/theme-modern.css';
	// If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
	import '@skeletonlabs/skeleton/styles/all.css';
	// Most of your app wide CSS should be put in this file
	import '../app.postcss';

	import { AppShell, AppBar, LightSwitch } from '@skeletonlabs/skeleton';
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
			
	<button type="button" class="btn variant-ghost-primary">
		<span>(icon)</span>
		<span>About</span>
	</button>
	<button type="button" class="btn variant-ghost-primary">
		<span>(icon)</span>
		<span>Past Projects</span>
	</button>
	<button type="button" class="btn variant-ghost-primary">
		<span>(icon)</span>
		<span>Skills</span>
	</button>
	<button type="button" class="btn variant-ghost-primary">
		<span>(icon)</span>
		<span>Contact</span>
	</button>

	<LightSwitch />
		</svelte:fragment>
	</AppBar>

	</svelte:fragment>
	<!-- Router Slot -->
	<slot />
	<!-- ---- / ---- -->
	<svelte:fragment slot="pageFooter">Page Footer</svelte:fragment>
</AppShell>